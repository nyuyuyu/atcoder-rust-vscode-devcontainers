FROM rust:1.70-bookworm
RUN cargo install cargo-compete

FROM mcr.microsoft.com/devcontainers/base:bookworm
COPY --from=0 /usr/local/cargo/bin/cargo-compete /usr/local/bin/
