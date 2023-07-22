### Сборка образа

```
docker image build ./ --tag stockproducts:1.0
```

### Запуск контейнера

```
docker run --name my_stockproducts -d -p 8000:8000 stockproducts:0.0.1
```
