## Практические задания

1. Создать кастомный хук *useWindowSize*, который будет отслеживать изменения размеров окна браузера и предоставлять текущую ширину и высоту окна.

#### Требования:
##### Создание Кастомного Хука:
Хук useWindowSize должен возвращать текущее значение ширины и высоты окна браузера.
Хук должен обновлять значения при изменении размера окна.
##### Функциональность Хука:
Используйте событие resize для отслеживания изменений размера окна.
Обновляйте значения ширины и высоты в состоянии компонента при каждом изменении размера окна.
##### Пример Использования:
Создайте компонент, который использует хук useWindowSize для отображения текущих размеров окна.
Компонент должен обновлять отображаемые размеры в реальном времени при изменении размеров окна.
На выходе должно получиться 2 файла. В одном лежит хук, в другом пример компонента, где будет использоваться этот хук

2. Найдите ошибку в коде и предложите вариант исправления.
```
import React, { useState } from 'react';

const UserList = ({ users }) => {
  const [search, setSearch] = useState('');
  const [filteredUsers, setFilteredUsers] = useState(users);

  const handleSearchChange = (e) => {
    setSearch(e.target.value);
    setFilteredUsers(users.filter(user => 
      user.name.toLowerCase().includes(e.target.value.toLowerCase())
    ));
  };

  return (
    <div>
      <input
        type="text"
        value={search}
        onChange={handleSearchChange}
        placeholder="Search users..."
      />
      <ul>
        {filteredUsers.map(user => (
          <li key={user.id}>{user.name}</li>
        ))}
      </ul>
    </div>
  );
};

const App = () => {
  const users = [
    { id: 1, name: 'Alice' },
    { id: 2, name: 'Bob' },
    { id: 3, name: 'Charlie' }
  ];

  return (
    <div>
      <h1>User List</h1>
      <UserList users={users} />
    </div>
  );
};

export default App;
```



3. Написать любой компонент выпадающего списка. 
<h1 align="center">
  Удачи! <a href="https://www.youtube.com/channel/UCaW0RNRwMILFdRM3-EpUYjg" target="_blank">😉</a> 
</h1>
