# react-native-iran-region-picker

IOS & Android.

a modal picker(wheel) of Iran province & city & region.

## propTypes
```
isRtl: PropTypes.bool,
isVisible: PropTypes.bool,
isShowArea: PropTypes.bool,
selectedProvince: PropTypes.string,
selectedCity: PropTypes.string,
selectedArea: PropTypes.string,
navBtnColor: PropTypes.string,
animationType: PropTypes.string,
transparent: PropTypes.bool,
onSubmit: PropTypes.func,
onCancel: PropTypes.func,
androidPickerHeight: PropTypes.number   
```

## Install
npm install react-native-iran-region-picker --save

## Usage
```javascript
import IranRegionWheelPicker from 'react-native-iran-region-picker';

// ios
<IranRegionWheelPicker
  onSubmit={(params) => this.setState({ region1: `${params.province},${params.city},${params.area}` })}
  onCancel={() => console.log('cancel')}
>
  <TextInput
    editable={false}
    placeholder="انتخاب منطقه"
    value={this.state.region1}
  />
</IranRegionWheelPicker>

// android
<IranRegionWheelPicker
  onSubmit={(params) => this.setState({ region1: `${params.province},${params.city},${params.area}` })}
  onCancel={() => console.log('cancel')}
>
  <Text
    style={{ backgroundColor: '#FFF', width: 200, paddingVertical: 20, textAlign: 'center', color: 'black' }}
  >{this.state.region1 || 'انتخاب منطقه'}</Text>
</IranRegionWheelPicker>

//Example:index.ios.js/android.ios.js
<IranRegionWheelPicker
  isVisible={this.state.isPickerVisible}
  navBtnColor={'red'}
  selectedProvince={'تهران'}
  selectedCity={'تهران'}
  selectedArea={'تجریش'}
  transparent
  animationType={'fade'}
  onSubmit={this._onPressSubmit.bind(this)}
  onCancel={this._onPressCancel.bind(this)}
  androidPickerHeight={100}
/>

<TouchableOpacity
  onPress={this._onPress2Show.bind(this)}
>
  <Text style={{ color: 'white' }}>{this.state.region2 || 'انتخاب منطقه' }</Text>
</TouchableOpacity>

```

# react-native-iran-region-picker
