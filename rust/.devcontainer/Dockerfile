# Use an official lightweight base image
FROM --platform=linux/amd64 rust:1.70-bullseye

# Install necessary tools
RUN apt-get update && apt-get install -y \
	build-essential \
	curl \
	gcc \
	gdb \
	lldb \
	git \
	pkg-config \
	zsh \
	&& rm -rf /var/lib/apt/lists/* 

RUN rustup target add x86_64-unknown-none
RUN rustup default stable
RUN rustup component add rust-src
RUN rustup component add rustfmt
RUN rustup component add clippy
