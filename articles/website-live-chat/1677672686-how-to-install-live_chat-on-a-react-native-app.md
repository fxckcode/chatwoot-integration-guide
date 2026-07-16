# How to install live-chat on a React Native app?

If you have a React Native app, you can add Chatwoot live chat widget and talk to your visitors in real-time. This can be done in 3 simple steps using the Chatwoot plugin.

## Step 1. Create a website inbox in Chatwoot​

Please refer to this [guide](https://app.chatwoot.com/hc/chatwoot-user-guide-cloud-version/en/website-live-chat/474) for detailed instructions on setting a website inbox in Chatwoot.

## Step 2. Add the plugin to your project[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/react-native-widget#2-add-the-plugin-to-your-project "Direct link to heading")

Add one of the following plugins to your project.

```
yarn add @chatwoot/react-native-widget
```

or

```
npm install --save @chatwoot/react-native-widget --save
```

This library depends on [react-native-webview](https://www.npmjs.com/package/react-native-webview) and [async-storage](https://github.com/react-native-async-storage/async-storage). Please follow the instructions provided in the docs.

**iOS Installation**[**​**](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/react-native-widget#ios-installation "Direct link to heading")

If you're using React Native versions > 60.0, it's relatively straightforward.

```
cd ios && pod install
```

## Step 3. Use it like this[​](https://www.chatwoot.com/docs/product/channels/live-chat/integrations/react-native-widget#3-use-it-like-this "Direct link to heading")

Replace `websiteToken` and `baseUrl` with appropriate values.

```
import React, { useState } from 'react';
import { StyleSheet, View, SafeAreaView, TouchableOpacity, Text } from 'react-native';
import ChatWootWidget from '@chatwoot/react-native-widget';

const App = () => {
  const [showWidget, toggleWidget] = useState(false);
  const user = {
    identifier: 'john@gmail.com',
    name: 'John Samuel',
    avatar_url: '',
    email: 'john@gmail.com',
    identifier_hash: '',
  };
  const customAttributes = { accountId: 1, pricingPlan: 'paid', status: 'active' };
  const websiteToken = 'WEBSITE_TOKEN';
  const baseUrl = 'CHATWOOT_INSTALLATION_URL';
  const locale = 'en';

  return (
    <SafeAreaView style={styles.container}>
      <View>
        <TouchableOpacity style={styles.button} onPress={() => toggleWidget(true)}>
          <Text style={styles.buttonText}>Open widget</Text>
        </TouchableOpacity>
      </View>
      {
        showWidget&&
          <ChatWootWidget
            websiteToken={websiteToken}
            locale={locale}
            baseUrl={baseUrl}
            closeModal={() => toggleWidget(false)}
            isModalVisible={showWidget}
            user={user}
            customAttributes={customAttributes}
          />
      }

    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
  },

  button: {
    height: 48,
    marginTop: 32,
    paddingTop: 8,
    paddingBottom: 8,
    backgroundColor: '#1F93FF',
    borderRadius: 8,
    borderWidth: 1,
    borderColor: '#fff',
    justifyContent: 'center',
  },
  buttonText: {
    color: '#fff',
    textAlign: 'center',
    paddingLeft: 10,
    fontWeight: '600',
    fontSize: 16,
    paddingRight: 10,
  },
});

export default App;
```

And...you're done. Check out the complete example [here](https://github.com/chatwoot/chatwoot-react-native-widget/tree/develop/examples).
