---
title: "Добавить правило-исключение WAF"
description: "Следуя данной инструкции, вы сможете создать правило-исключение для WAF."
---

# Добавить правило-исключение WAF

{% list tabs group=instructions %}

- Консоль управления {#console}

  1. В [консоли управления]({{ link-console-main }}) выберите каталог с профилем WAF.
  1. В списке сервисов выберите **{{ ui-key.yacloud.iam.folder.dashboard.label_smartwebsecurity }}**.
  1. Перейдите на вкладку ![image](../../_assets/smartwebsecurity/waf.svg) **Профили WAF**.
  1. Выберите профиль, в который вы хотите добавить [правило-исключение](../concepts/waf.md#exclusion-rules).
  1. Перейдите на вкладку ![image](../../_assets/console-icons/file-xmark.svg) **Правила-исключения** и нажмите кнопку **Создать правило-исключение**.
  1. Введите имя правила-исключения.
  1. (опционально) Введите описание.
  1. В блоке **Область применения** укажите правила из базового набора, для которых будет срабатывать исключение:
     1. **Все правила**.
     1. **Выбранные правила** — нажмите **Добавить правила** и выберите правила из базового набора.
  1. В блоке **Условия на трафик** выберите [условия](../concepts/conditions.md) для срабатывания правила-исключения.

      Если оставить поле **Условия** пустым, правило-исключение будет применено ко всему трафику.
  1. Нажмите кнопку **Создать**.

{% endlist %}


### См. также {#see-also}

* [{#T}](configure-set-rules.md)
* [{#T}](exclusion-rule-delete.md)
* [{#T}](rule-add.md)