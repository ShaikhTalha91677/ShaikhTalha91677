import React, { useState } from 'react';
import { View, Text, TextInput, Button } from 'react-native';

const ExpertsOnDataLoginSignupScreen = () => {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = () => {
    // TODO: Implement login functionality
  };

  const handleSignup = () => {
    // TODO: Implement signup functionality
  };

  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
      <Text style={{ fontSize: 24 }}>Welcome to Experts on Data!</Text>
      <Text style={{ fontSize: 16 }}>Login or Signup</Text>
      <TextInput
        style={{ borderWidth: 1, borderColor: '#ccc', padding: 10, margin: 10 }}
        placeholder="Username"
        value={username}
        onChangeText={(text) => setUsername(text)}
      />
      <TextInput
        style={{ borderWidth: 1, borderColor: '#ccc', padding: 10, margin: 10 }}
        placeholder="Password"
        secureTextEntry
        value={password}
        onChangeText={(text) => setPassword(text)}
      />
      <Button title="Login" onPress={handleLogin} />
      <Button title="Signup" onPress={handleSignup} />
    </View>
  );
};

export default ExpertsOnDataLoginSignupScreen;

import AsyncStorage from '@react-native-community/async-storage';

const saveLoginData = async (username, password) => {
  try {
    await AsyncStorage.setItem('username', username);
    await AsyncStorage.setItem('password', password);
  } catch (error) {
    // TODO: Handle error
  }
};

const handleLogin = () => {
  const username = state.username;
  const password = state.password;

  saveLoginData(username, password);

  // TODO: Navigate to the next screen
};

