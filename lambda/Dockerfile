# Base image for Python 3.9 Lambda
FROM public.ecr.aws/lambda/python:3.9

# Set working directory to Lambda task root
WORKDIR ${LAMBDA_TASK_ROOT}

# Copy function code and dependencies
COPY app.py ./
COPY requirements.txt ./

# Install dependencies into the Lambda task root
RUN pip install --no-cache-dir -r requirements.txt --target .

# Set Lambda function handler (filename.function_name)
CMD ["app.lambda_handler"]
