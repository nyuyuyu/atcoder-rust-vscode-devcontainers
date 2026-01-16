FROM rust:1.89-bookworm
RUN cargo install --locked --git https://github.com/nyuyuyu/cargo-compete.git --branch feature/support-rust-2024

FROM mcr.microsoft.com/devcontainers/base:bookworm
COPY --from=0 /usr/local/cargo/bin/cargo-compete /usr/local/bin/
