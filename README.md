Simply add the component and pass in the props.

Example.

import Notifications from "../Notifications";

const [errors, setErrors] = useState([]);

const errorElements = () =>
errors.map((error, i) => <div key={i}>{error}</div>);

Alert message
<Notifications
type={"alert"}
variant={"danger"}
heading={"Error"}
body={errorElements()}
/>

Toast Message
<Notifications
type={"alert"}
heading={"Error"}
small={"please try again"}
body={errorElements()}
/>
