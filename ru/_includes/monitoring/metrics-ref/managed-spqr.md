Имя метрики пишется в метку `name`.

Общие метки для всех метрик сервиса {{ mpg-name }}:

Метка | Значение
----|----
service | Идентификатор сервиса: `managed-spqr`
resource_type | Тип ресурса: `cluster`
resource_id | Идентификатор кластера
host | FQDN хоста
subcluster_name | Имя подкластера

## Метрики CPU {#managed-spqr-cpu-metrics}
Загрузка процессорных ядер.

| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `cpu.guest`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `guest`. | 
| `cpu.idle`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `idle`. | 
| `cpu.iowait`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `iowait`. | 
| `cpu.irq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `irq`. | 
| `cpu.nice`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `nice`. | 
| `cpu.softirq`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `softirq`. | 
| `cpu.steal`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `steal`. | 
| `cpu.system`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `system`. | 
| `cpu.user`<br/>`DGAUGE`, % | Использование процессорных ядер, тип потребления `user`. |
| `load.avg_15min`<br/>`DGAUGE`, % | Средняя нагрузка за 15 минут. | 
| `load.avg_1min`<br/>`DGAUGE`, % | Средняя нагрузка за 1 минуту. | 
| `load.avg_5min`<br/>`DGAUGE`, % | Средняя нагрузка за 5 минут. |
| `pg_backend_cpu`<br/>`DGAUGE`, % | Утилизация CPU процессом {{ PG }}. |

## Метрики диска {#managed-spqr-disk-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `disk.free_bytes`<br/>`DGAUGE`, байты | Свободное место. | 
| `disk.free_inodes`<br/>`DGAUGE`, штуки | Свободное количество inodes. | 
| `disk.temp_files_size`<br/>`DGAUGE`, байты | Размер временных файлов. | 
| `disk.total_bytes`<br/>`DGAUGE`, байты | Доступное место. | 
| `disk.total_inodes`<br/>`DGAUGE`, штуки | Доступное количество inodes. | 
| `disk.used_bytes`<br/>`DGAUGE`, байты | Занятое место. | 
| `disk.used_inodes`<br/>`DGAUGE`, штуки | Занятое количество inodes. |
| `disk.wal_size`<br/>`DGAUGE`, байты | Размер журнала упреждающей записи. |
| `pg_backend_read_bytes`<br>`DGAUGE`, байты/с | Скорость чтения данных процессом {{ PG }}. |
| `pg_backend_write_bytes`<br>`DGAUGE`, байты/с | Скорость записи данных процессом {{ PG }}. |

## Метрики дисковых операций {#managed-spqr-diskio-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `io.avg_read_time`<br/>`DGAUGE`, миллисекунды | Среднее время чтения с дисков. | 
| `io.avg_write_time`<br/>`DGAUGE`, миллисекунды | Среднее время записи на диски. | 
| `io.disk*.avg_read_time`<br/>`DGAUGE`, миллисекунды | Среднее время чтения с конкретного диска. | 
| `io.disk*.avg_write_time`<br/>`DGAUGE`, миллисекунды | Среднее время записи на конкретный диск. | 
| `io.disk*.read_bytes`<br/>`DGAUGE`, байт/с | Скорость чтения с конкретного диска. | 
| `io.disk*.read_count`<br/>`DGAUGE`, операций/с | Количество операций чтения с конкретного диска в секунду. | 
| `io.disk*.read_merged_count`<br/>`DGAUGE`, операций/с | Количество слитых операций чтения с конкретного диска в секунду. | 
| `io.disk*.utilization`<br/>`DGAUGE`, % | Использование конкретного диска. Не работает для сетевых дисков. | 
| `io.disk*.write_bytes`<br/>`DGAUGE`, байт/с | Скорость записи на конкретный диск. | 
| `io.disk*.write_count`<br/>`DGAUGE`, операций/с | Количество операций записи на конкретный диск в секунду. | 
| `io.disk*.write_merged_count`<br/>`DGAUGE`, операций/с | Количество слитых операций записи на конкретный диск в секунду. |
| `io.read_bytes`<br/>`DGAUGE`, байт/с | Скорость чтения с дисков. | 
| `io.read_count`<br/>`DGAUGE`, операций/с | Количество операций чтения в секунду. | 
| `io.read_merged_count`<br/>`DGAUGE`, операций/с | Количество слитых операций чтения в секунду. | 
| `io.utilization`<br/>`DGAUGE`, % | Использование дисков. | 
| `io.write_bytes`<br/>`DGAUGE`, байт/с | Скорость записи на диски. | 
| `io.write_count`<br/>`DGAUGE`, операций/с | Количество операций записи в секунду. | 
| `io.write_merged_count`<br/>`DGAUGE`, операций/с | Количество слитых операций записи в секунду. |

## Метрики RAM {#managed-spqr-ram-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `mem.active_bytes`<br/>`DGAUGE`, байты | Объем оперативной памяти, которая используется наиболее часто и освобождается только в крайнем случае. | 
| `mem.available_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `available`. | 
| `mem.buffers_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `buffers`. | 
| `mem.cached_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `cached`. | 
| `mem.free_bytes`<br/>`DGAUGE`, байты | Объем свободной оперативной памяти, доступной для использования, без учета `mem.buffers_bytes` и `mem.cached_bytes`. |
| `mem.shared_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `shared`. | 
| `mem.total_bytes`<br/>`DGAUGE`, байты | Использование оперативной памяти, тип потребления `total`. | 
| `mem.used_bytes`<br/>`DGAUGE`, байты | Объем оперативной памяти, которую в данный момент используют запущенные процессы. | 
| `oom_count`<br/>`DGAUGE`, штуки | Количество случаев нехватки памяти. |

## Метрики сети {#managed-spqr-net-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `net.bytes_recv`<br/>`DGAUGE`, байт/с | Скорость получения данных по сети. | 
| `net.bytes_sent`<br/>`DGAUGE`, байт/с | Скорость отправки данных по сети. | 
| `net.dropin`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при получении. | 
| `net.dropout`<br/>`DGAUGE`, штуки | Количество пакетов, отброшенных при отправке. | 
| `net.errin`<br/>`DGAUGE`, штуки | Количество ошибок при получении. | 
| `net.errout`<br/>`DGAUGE`, штуки | Количество ошибок при отправке. | 
| `net.packets_recv`<br/>`DGAUGE`, пакетов/с | Интенсивность получения данных по сети. | 
| `net.packets_sent`<br/>`DGAUGE`, пакетов/с | Интенсивность отправки данных по сети. |

## Метрики сервиса {#managed-spqr-metrics}
#### Метрики кластера {#managed-spqr-cluster-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `spqr_health.spqr-is_alive`<br/>`DGAUGE`, 0/1 | Показатель работоспособности хоста.<br/>Принимает значение `1`, если хост SPQR работает, `0`, если нет. | 

#### Метрики роутера {#managed-spqr-router-metrics}
| Имя<br/>Тип, единицы измерения | Описание |
| ----- | ----- |
| `spqr_router_stats.clients_count`<br/>`DGAUGE`, штуки | Количество клиентов в роутере. | 
| `spqr_router_stats.connections_count`<br/>`DGAUGE`, штуки | Количество соединений между роутером и шардами. |