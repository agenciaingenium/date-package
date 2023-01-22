# date-package
Opción 1

```
$meses = array();
$mes = new DateTime('first day of January');
for ($i = 1; $i <= 12; $i++) {
    $meses[] = $mes->format('F');
    $mes->modify('first day of next month');
}
print_r($meses);
```

Opción 2
```
$meses = array();
for ($i = 1; $i <= 12; $i++) {
    $meses[] = date("F", mktime(0, 0, 0, $i, 1));
}
print_r($meses);
```
