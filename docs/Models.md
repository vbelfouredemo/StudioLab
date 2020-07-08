# Models

## Step #1

Create stand alone `json` files for the following models:


### User
**Description**: *Users associated with a CloudHome account. Administrative priviledges are indicated to show which users can configure device management and which users can only interact with configured devices.*

![user model](../assets/images/user.png)

### Account
**Description**: *Users can belong to multiple accounts on CloudHome's federated services. In other words users have a unique id that can interact or manage devices on more than one account or location.*

![account model](../assets/images/account.png)

### Location
**Description**: *Device geolocation at most recent update. Users can optionally choose to turn off geolocation, however key features such as mapping will not be available.*

![location model](../assets/images/location.png)