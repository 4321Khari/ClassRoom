## Technologies Used

- Frontend: React.js, Material UI, Redux
- Backend: Node.js, Express.js
- Database: MongoDB

<br>
<br/>


# Installation

```sh
git clone https://github.com/4321Khari/ClassRoom.git
```
Open 2 terminals in separate windows/tabs.

Terminal 1: Setting Up Backend 
```sh
cd backend
npm install
npm start
```

Create a file called .env in the backend folder.
Inside it write this :

```sh
MONGO_URL = mongodb://127.0.0.1/school
```
If you are using MongoDB Compass you can use this database link but if you are using MongoDB Atlas then instead of this link write your own database link.

Terminal 2: Setting Up Frontend
```sh
cd frontend
npm install
npm start
```
Now, navigate to `localhost:3000` in your browser. 
The Backend API will be running at `localhost:5000`.
<br>
# Error Solution

You might encounter an error while signing up, either a network error or a loading error that goes on indefinitely.

To resolve it:

1. Navigate to the `frontend > .env` file.

2. Uncomment the first line. After that, terminate the frontend terminal. Open a new terminal and execute the following commands:
```sh
cd frontend
npm start
```

After completing these steps, try signing up again. If the issue persists, follow these additional steps to resolve it:

1. Navigate to the `frontend > src > redux > userRelated > userHandle.js` file.

2. Add the following line after the import statements:

```javascript
const REACT_APP_BASE_URL = "http://localhost:5000";
```

3. Replace all instances of `process.env.REACT_APP_BASE_URL` with `REACT_APP_BASE_URL`.

**IMPORTANT:** Repeat the same process for all other files with "Handle" in their names.

For example, in the `redux` folder, there are other folders like `userRelated`. In the `teacherRelated` folder, you'll find a file named `teacherHandle`. Similarly, other folders contain files with "Handle" in their names. Make sure to update these files as well.

The issue arises because the `.env` file in the frontend may not work for all users, while it works for me.


 
 
