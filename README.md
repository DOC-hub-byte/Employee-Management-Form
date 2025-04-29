# Employee-Management-Form
INT304: Web Design &amp; Development (Learning React App)

// Added code to App.js to store employee data
useEffect(() => {
  const storedEmployees = localStorage.getItem('employees');
  if (storedEmployees) {
    setEmployees(JSON.parse(storedEmployees)); 
  }
}, []); 

// Added code to App.js to save employee data
  useEffect(() => {
    saveData(employees);
  }, [employees]);

  const saveData = (data) => {
    localStorage.setItem('employees', JSON.stringify(data));
  };
