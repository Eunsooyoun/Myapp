### Myapp
```java
import React, { Component } from 'react';
import { List,Divider, Container, Header, Breadcrumb, Button, Grid, Dropdown } from 'semantic-ui-react';

class Mymenu extends Component{
    render(){
        const items = [
            { key: 'plate', text: 'Plate', value: 'plate' },
            { key: 'hotcoil', text: 'HotCoil', value: 'hotcoil' },
          ]
        return(
        <div>
        <Header as='h3' block textAlign='center'>
            CTQ 모니터링
        </Header>
        <Container>
        <Grid columns='equal'>
            <Grid.Column>
                    <Breadcrumb size='tiny' floated='right'>
                    <Breadcrumb.Section link>1depth 메뉴명</Breadcrumb.Section>
                    <Breadcrumb.Divider icon='right angle' />
                    <Breadcrumb.Section link>2depth 메뉴명</Breadcrumb.Section>
                    <Breadcrumb.Divider icon='right angle' />
                    <Breadcrumb.Section active>CTQ-Vital Few 상세 Data 조회 </Breadcrumb.Section>
                    </Breadcrumb>

                    <Button size='mini' floated='right'>P 인쇄</Button>
                    <Button size='mini' floated='right'># 엑셀 다운로드</Button>
                    <Button size='mini' floated='right'>? 도움</Button>
            </Grid.Column>
        </Grid>
        <Divider hidden />
            <Header as='h3' block>
                품질지표 모니터링 Report 조회
            </Header>
        <Divider hidden />
        <Grid reversed='tablet' columns='equal'>
        <List horizontal>
            <List.Item>
                <List.Content verticalAlign='middle'>제품</List.Content>
            </List.Item>
            <List.Item>
                <Dropdown compact placeholder='제품' search selection options={items} />
            </List.Item>
            <List.Item>
                <List.Content verticalAlign='middle'>사용자</List.Content>
            </List.Item>
            <List.Item>
                <Dropdown compact placeholder='사용자' search selection options={items} />
            </List.Item>
            <List.Item>
                <List.Content verticalAlign='middle'>CTQ명</List.Content>
            </List.Item>
            <List.Item>
                <Dropdown compact placeholder='CTQ명' search selection options={items} />
            </List.Item>
            <List.Item>
                <List.Content verticalAlign='middle'>주기</List.Content>
            </List.Item>
            <List.Item>
                <Dropdown compact placeholder='주기' search selection options={items} />
            </List.Item>
            <List.Item>
                <List.Content verticalAlign='middle'>기준일</List.Content>
            </List.Item>
            <List.Item>
                <Dropdown compact placeholder='YYYY-MM-DD' search selection options={items} />
            </List.Item>
        </List>
            <List.Item>
                <Button size='normal' color='blue'  floated='right'>조회</Button>
            </List.Item>
              </Grid>
            </Container>
        </div>
        )
    }
}

export default Mymenu;

```


### App.js
```java
import React, { Component } from 'react';
import Mymenu from './component/Mymenu';


class App extends Component {
  render() {
    return (
      <div className="App">
        <header className="App-header">
          <Mymenu/>
        </header>
      </div>
    );
  }
}

export default App;
```

### index.js
```java
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';
import 'semantic-ui-css/semantic.min.css';

ReactDOM.render(<App />, document.getElementById('root'));

// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: http://bit.ly/CRA-PWA

```
