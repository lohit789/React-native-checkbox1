react-native-check-box
Checkbox component for react native, it works on iOS and Android.

Content
Installation
Demo
Getting started
API
Contribution
Changes
For React Native >= 0.54 use v2.1.2+, for React Native < 0.4.4 use v1.0.4

Installation
1.Run npm i react-native-check-box --save
2.import CheckBox from 'react-native-check-box'
Demo
Examples
Screenshots

Getting started
Add react-native-check-box to your js file.

import CheckBox from 'react-native-check-box'

Inside your component's render method, use CheckBox:

<CheckBox
    style={{flex: 1, padding: 10}}
    onClick={()=>{
      this.setState({
          isChecked:!this.state.isChecked
      })
    }}
    isChecked={this.state.isChecked}
    leftText={"CheckBox"}
/>
Then you can use it like this:

Basic usage
<CheckBox
    style={{flex: 1, padding: 10}}
    onClick={()=>{
      this.setState({
          isChecked:!this.state.isChecked
      })
    }}
    isChecked={this.state.isChecked}
    leftText={"CheckBox"}
/>
Custom CheckBox
renderCheckBox(data) {
    var leftText = data.name;
    return (
        <CheckBox
            style={{flex: 1, padding: 10}}
            onClick={()=>{
                 this.setState({
                     isChecked:!this.state.isChecked
                 })
               }}
            isChecked={this.state.isChecked}
            checkedImage={<Image source={require('../../page/my/img/ic_check_box.png')} style={this.props.theme.styles.tabBarSelectedIcon}/>}
            unCheckedImage={<Image source={require('../../page/my/img/ic_check_box_outline_blank.png')} style={this.props.theme.styles.tabBarSelectedIcon}/>}
        />);
}
More Usage:

GitHubPopular

API
Props	Type	Optional	Default	Description
style	ViewPropTypes.style	true		Custom style checkbox
leftText	PropTypes.string	true		Custom left Text
leftTextStyle	Text.propTypes.style	true		Custom left Text style
rightText	PropTypes.string	true		Custom right Text
rightTextView	PropTypes.element	true		Custom right TextView
rightTextStyle	Text.propTypes.style	true		Custom right Text style
checkedImage	PropTypes.element	true	Default image	Custom checked Image
unCheckedImage	PropTypes.element	true	Default image	Custom unchecked Image
isChecked	PropTypes.bool	false	false	checkbox checked state
onClick	PropTypes.func.isRequired	false		callback function
disabled	PropTypes.bool	true	false	Disable the checkbox button
checkBoxColor	PropTypes.string	true		Tint color of the checkbox image (this props is for both checked and unchecked state)
checkedCheckBoxColor	PropTypes.string	true		Tint color of the checked state checkbox image (this prop will override value of checkBoxColor for checked state)
uncheckedCheckBoxColor	PropTypes.string	true		Tint color of the unchecked state checkbox image (this prop will override value of checkBoxColor for unchecked state)
Contribution
Issues are welcome. Please add a screenshot of bug and code snippet. Quickest way to solve issue is to reproduce it on one of the examples.

Pull requests are welcome. If you want to change API or making something big better to create issue and discuss it first.
