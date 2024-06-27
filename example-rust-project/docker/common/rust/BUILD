docker_image(
    name="dev-common-rust",
    description="base rust image for dev environment",
    tags=["example-rust-project", "dev-image", "dev-common-image"],
    source="Dockerfile",
    image_tags=["{build_args.GIT_CURRENT_BRANCH}"],
    target_stage="dev",
    dependencies=["example-rust-project/docker/common/ubuntu:dev-common-ubuntu", ":build"],
    extra_build_args=["TARGET=dev", "RUST_VERSION=1.79.0"],
)

file(name="build", source="BUILD")
