# This is a Dockerfile for a JDBC driver add-on for EAP.

FROM scratch

# Labels
LABEL name="PosgreSQL JDBC Driver" \
      version="42.2.24"

# Copy add-on details
COPY install.sh \
     install.properties \
     /extensions/
COPY modules /extensions/modules/

# Download the driver into the module folder
ADD https://jdbc.postgresql.org/download/postgresql-42.2.24.jar \
    /extensions/modules/system/layers/openshift/org/postgresql/main/
