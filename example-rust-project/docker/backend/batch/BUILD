docker_image(
    name="dev-backend-batch",
    description="backend batch server image for dev environment",
    tags=["example-rust-project", "dev-image", "dev-backend-image"],
    source="Dockerfile",
    image_tags=["{build_args.GIT_CURRENT_BRANCH}"],
    target_stage="dev",
    dependencies=[
        "example-rust-project/docker/common/rust:dev-common-rust",
        ":build",
        ":vscode-extensions",
    ],
    extra_build_args=[
        "TARGET=dev",
        "DOCKER_FILE_PATH=./example-rust-project/docker/backend/batch",
        "VSCODE_EXTENSIONS_JSON=extensions.json",
        "APP_DIR=app",
        "PORT=8082",
    ],
)

file(name="build", source="BUILD")
file(name="vscode-extensions", source="extensions.json")
