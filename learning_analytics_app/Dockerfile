FROM python:3.12-slim

WORKDIR /code

COPY . /code/

RUN pip install uv

# Install dependencies exact versions specified in pyproject.toml
RUN uv sync --frozen

EXPOSE 8000

CMD ["uv", "run", "uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]