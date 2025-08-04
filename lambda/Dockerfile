FROM public.ecr.aws/lambda/python:3.9

# Copy function code
COPY app.py ./
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Set the CMD to your handler (filename.function_name)
CMD ["app.lambda_handler"]
