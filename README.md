# lab11_axios_example

1.	create react app and GitHub repository having name lab11_StudentID_axios_example

2.	Install required packages using following command

	npm install --save axios
	npm install --save react-bootstrap bootstrap

3.	Create the PersonList components to fetch data using axios. 
Paste following code inside the PersonList component to fetch data from given API. Below is the reference code

//Define state default values
    state = {
        persons: []
    }

     //Component Lifecycle Callback
    componentDidMount() {
        axios.get(`https://randomuser.me/api/?results=10`)
        .then(res => {
            console.log(res.data);
            const persons = res.data.results;
            this.setState({ persons });
        })
    }

4.	Try to get data using JS fetch or axios API
