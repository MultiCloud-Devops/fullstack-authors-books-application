# Dockerfile - buildah-awscli image
FROM quay.io/buildah/stable

# Install AWS CLI v2
RUN yum install -y unzip curl && \
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install && \
    rm -rf awscliv2.zip aws

# Confirm install
RUN aws --version && buildah --version
