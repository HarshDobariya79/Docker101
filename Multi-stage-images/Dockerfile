# Stage 1: Build Stage
FROM gcc:latest as builder

# Set the working directory
WORKDIR /app

# Copy the source code
COPY . .

# Build the C++ program
# static compilation is the most important thing. Check `$ ldd <compiled_file_name>` for dynamic links
RUN g++ -o executable_file app.cpp -static

# Stage 2: Production Stage
FROM scratch

# Set the working directory
WORKDIR /app

# Copy only the necessary files from the build stage
COPY --from=builder /app/executable_file .

# Run the compiled C++ program
CMD ["./executable_file"]