## Основная часть

Необходимо создать собственные workflow для двух типов задач: bug и остальные типы задач. Задачи типа bug должны проходить жизненный цикл:

1. Open -> On reproduce.
2. On reproduce -> Open, Done reproduce.
3. Done reproduce -> On fix.
4. On fix -> On reproduce, Done fix.
5. Done fix -> On test.
6. On test -> On fix, Done.
7. Done -> Closed, Open.

![bug_workflow](./task/bug_workflow.png)

Остальные задачи должны проходить по упрощённому workflow:

1. Open -> On develop.
2. On develop -> Open, Done develop.
3. Done develop -> On test.
4. On test -> On develop, Done.
5. Done -> Closed, Open.

![task_workflow](./task/task_workflow.png)

## Что нужно сделать

1. Создайте задачу с типом bug, попытайтесь провести его по всему workflow до Done.

![bug_kanban0](./task/bug_kanban0.png)
![bug_kanban2](./task/bug_kanban2.png)
![bug_done](./task/bug_done.png)

2. Создайте задачу с типом epic, к ней привяжите несколько задач с типом task, проведите их по всему workflow до Done.

![epic_task](./task/epic_task.png)

3. При проведении обеих задач по статусам используйте kanban.
4. Верните задачи в статус Open.

![bug_kanban1](./task/bug_kanban1.png)
![epic_task](./task/epic_task.png)

5. Перейдите в Scrum, запланируйте новый спринт, состоящий из задач эпика и одного бага, стартуйте спринт, проведите задачи до состояния Closed. Закройте спринт.

![sprint](./task/sprint.png)
![sprint_start](./task/sprint_start.png)
![sprint_closed](./task/scrum_closed.png)

6. Если всё отработалось в рамках ожидания — выгрузите схемы workflow для импорта в XML. Файлы с workflow и скриншоты workflow приложите к решению задания.

>Ответ: [bug.xml](./task/bug_workflow.xml), [other](./task/task_workflow.xml)
