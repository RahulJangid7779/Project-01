// const { adminauth } = require("./middlewares" / "auth");
// this mean that we create the application
// this is overwrite all the other router
// app.use("/test", (req, res) => {
// res.send("hello from the server");
// });
// this will only handle GET call to /user
// app.get("/user/:userId", (req, res) => {
// console.log(req.query());
// res.send({ firstname: "rahul", lastname: "saini" });
// });
//this will only handle post call to /user
// app.post("/user", (req, res) => {
// res.send("Data is succesfully saved to the database");
// });
// this will only handle delete call to user
// app.delete("/user", (req, res) => {
// res.send("Data is delete successfully");
// });
// app.get("/ab?c", (req, res) => {
// res.send(" HELLO THERE IS NEW DATA");
// }); // here ? mean that if we call the api usig /abc it will give output and if we use /ac it will also give me the same output
//
// app.get("/ab+c", (req, res) => {
// res.send(" HELLO THERE IS NEW DATA");
// });
// /abc it will work if we write /ab+c it will give me output for abbbbbbbbbc also
// app.get("/ab\*c", (req, res) => {
// res.send(" HELLO THERE IS NEW DATA");
// }); //it mean that if we write abRAHUKc it will work we can write in between any thiing
// app.get("/a(bc )", (req, res) => {
// res.send(" HELLO THERE IS NEW DATA");
// }); // it will give answer to a and in bracket bc is optional
// app.get("/a/", (req, res) => {
// res.send(" HELLO THERE IS NEW DATA");
// }); // thus mean that if in between /lllas it will work
// app.get("/user", (req, res) => {
// res.send({ firstname: "rahul", lastname: "saini" });
// });
// app.use("/", (req, res) => {
// res.send("Hello Rahul Bhai");
// });

// app.use(
// /_we can also pass route here the server ex like test our server only repose when it has localhost:3000/test_/ (
// req,
// res
// ) => {
// res.send("Hello froms the server");
// }
// );
// /user --> route 1 parameter
// (req,res)----> route handler 2 parameter
// there can be multiple route handler
// app.use("/user", [
// (req, res, next) => {
// console.log("handling the route user 1");
// next();
// res.send("response!!");
// // this next function give by express js
// }, // WHEN the next came first and then come response it will print second response and get the error. when one response send and we send second response again then it will create an error bec there is multiple request at the same time1
// (req, res, next) => {
// console.log("handling the route user 2");
// res.send("2nd Response !!");
// next();
// },
// (req, res, next) => {
// console.log("handling the route user 2");
// req.send("response 3");
// next();
// },
// ]);
// app.use("/user", (req, res) => {}); // the request is sending requests ... .....
// we can pass into array also

// // that why we use route handeler to handle the request beacuse request id sending
// app.get("/admin/getAllData", (req, response) => {
// // logic of checking if the request is authorized
// // res.send("all data sent");
// const token = "xyz";
// const isAdminAuthorized = token === "xyx";
// if (isAdminAuthorized) {
// res.send("ALL DATA SEND");
// } else {
// res.send(404).send("unauthorized request");
// }
// });
// app.get("/admin/deleteUser", (req, res) => {
// res.send("All data delete");
// });
// HANDLE AUTH MIDDLEWARE FOR ALL GET POST ,...request
// app.use("/admin", (req, res, next) => {
// console.log("Admin auth is getting check out");
// const token = "xyz";
// const isAdminAuthorized = token === "xyz";
// if (!isAdminAuthorized) {
// res.send("Unauthorized request");
// } else {
// next();
// }
// });
// app.use("/admin", adminauth);
// app.get("/admin/getAllData", (req, response) => {
// // logic of checking if the request is authorized
// res.send("all data sent");
// });
// app.get("/admin/deleteUser", (req, res) => {
// res.send("All data delete");
// });
// app.get("/user", adminauth, (req, res) => {
// res.send("all data send");
// });
// ERROR HANDLEING
// app.use("/getuserdata", (res, res) => {
// try {
// throw new Error("fafafc");
// res.send("user data send");
// } catch (err) {
// res.status(500).send("user data send");
// }
// });
// // When ever we get an error when we call the app.get/getuser its will expose lots of thing to handle this we create a new
// // routuing which contain error as a parameter and we pass this on the first
// app.use("/", (err, req, res, next) => {
// if (err) {
// res.status(500).send("somthing went wrong");
// }
// });

// this mean that we listen the server on port number 3000 and also take the callback
// npm i -g nodemon this insall nodemon by the help of this we do not have to close the server again an again manually it will automatically close this
// we we by mistakly delete our node module we don't have to panic we can reinstalled it by the command npm install
// git
// when we change the position of the route the answer will change
