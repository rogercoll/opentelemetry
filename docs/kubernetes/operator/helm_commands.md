helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts
helm repo update
helm upgrade --install --namespace opentelemetry-operator-system opentelemetry-kube-stack open-telemetry/opentelemetry-kube-stack \
--values 'https://raw.githubusercontent.com/elastic/opentelemetry/refs/heads/8.16/resources/kubernetes/operator/helm/values.yaml' \
--version 0.3.3
