docker_image(
    name="dev-backend-batch",
    description="backend batch server image for dev environment",
    tags=["example-nest-project", "dev-image", "dev-backend-image"],
    source="Dockerfile",
    image_tags=["{build_args.GIT_CURRENT_BRANCH}"],
    target_stage="dev",
    dependencies=[
        "example-nest-project/docker/common/mise:dev-common-mise",
        ":build",
        ":vscode-extensions",
    ],
    extra_build_args=[
        "TARGET=dev",
        "DOCKER_FILE_PATH=./example-nest-project/docker/backend/batch",
        "VSCODE_EXTENSIONS_JSON=extensions.json",
        "NODE_VERSION=20.14.0",
        "APP_DIR=app",
        "PORT=5173",
        "BACKEND_PROJECT_NAME=backend"
    ],
)

file(name="build", source="BUILD")
file(name="vscode-extensions", source="extensions.json")
