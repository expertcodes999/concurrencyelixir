FROM elixir:latest

# Install build dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    inotify-tools \
    git \
    && rm -rf /var/lib/apt/lists/*

# Install hex package manager and rebar
RUN mix local.hex --force && \
    mix local.rebar --force

WORKDIR /workspace

# Set environment variables
ENV MIX_HOME=/workspace/.mix