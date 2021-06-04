# Configuração cluster K8s com Ansible

Projeto do treinamento para instalação de um cluster Kubernetes utilizando o Ansible + AWS.

## Fases do projeto

- Provisioning => Criar as instâncias/vms para o nosso cluster.
- Install_K8s => Criação do cluster, etc.
- Deploy_app_v(1,2) => Deploy de uma aplicação exemplo

Observação: esse ambiente é somente para ser utilizada como base e não como produção, para testes estamos liberando a porta SSH 22 para internet (0.0.0.0). O código poderá ser melhorado futuramente.


- Provisioning

Dentro da pasta você terá todo o código para construção de 3 instancias na AWS, com SG e liberando as portas necessárias para comunicação do cluster.

- Install_K8s

Dentro da pasta você terá todo o código necessário para a construção do cluster K8s, juntamente com o deploy do Prometheus Operator para monitoramento do ambiente, utilizando o Helm. Obs: As instancias provisionadas, na etapa anterior, irão informar os IPs de cada uma delas. Faz necessário copiar os IPs para o arquivo "hosts" da playbook Install_K8s.


Deploy_app_v(1,2) => Deploy de uma aplicação exemplo. A mesma regra do arquivo hosts, se aplica aqui.


## License
[MIT](https://choosealicence.com/licenses/mit/)

```
