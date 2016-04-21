# Nordnet Component Kit

## Installation
TODO once this is in sinopia/github this is true, until then - not so much!

```bash
npm install --save nordnet-component-kit
```

## Usage
```javascript
import { Percent, Currency } from 'nordnet-component-kit';

// ... some code

<Percent value={ 0.23 } decimals={ 1 } />
<Currency value={ 45.345 } currency="SEK" />
```

## Documentation
For examples and full documentation see [TODO link to ghpages?](TODO link to ghpages?)

To run the documentation locally, to this:
```bash
# Go to the documentation directory
cd examples/documentation
# Link your local nordnet-component-kit
npm link nordnet-component-kit ../..
# Install dependancies
npm install
# Run the documentation
npm start
```

## Components
For some examples usages for each component, please see the Documentation section above.

### Number components
All of the components in this section use an underlying component `<Number />`. All props sent to either of these components are propagated down to Number, which means that all components also can take the props specified in Number.

#### Number
**In use:**
This component is *not* exported to public and is only here because of the above text.

#### Currency
**In use:**
```javascript
<Currency value={ 34.4442 } decimals={ 2 } currency="DKK" />
// 34.44 DKK
```

#### Percent
**In use:**
```javascript
<Percent value={ 90.44 } decimals={ 2 } suffixSeparator=" " />
// 90.44 %
```

#### Development
**In use:**
```javascript
<Development value={ -112.2334 } decimals={ 2 } />
// ▼ 112.23
<Development value={ 2.2333 } type="percentage" />
// ▲ 2.23%
```

### DateTime
If the iso flag is not specified this component act as a wrapper for `FormattedDate` or `FormattedRelative`. It passes on props to these underlying components and therefore all props that are valid for them are also valid here.

**In use:**
```javascript
<DateTime value={ new Date() } />
// 4/15/2016
<DateTime value={ new Date() } iso minute="numeric" />
// 2016-04-15 13:55
<DateTime value={ (new Date() - 24 * 60 * 60 * 1000) } format="numeric" type="relative" />
// 1 day ago
```

## License
TODO - only needed if published on github?
