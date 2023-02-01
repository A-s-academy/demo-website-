## javascript
import React from 'react';
import { makeStyles } from '@material-ui/core/styles';
import Drawer from '@material-ui/core/Drawer';
import AppBar from '@material-ui/core/AppBar';
import CssBaseline from '@material-ui/core/CssBaseline';
import Toolbar from '@material-ui/core/Toolbar';
import List from '@material-ui/core/List';
import Typography from '@material-ui/core/Typography';
import Divider from '@material-ui/core/Divider';
import ListItem from '@material-ui/core/ListItem';
import ListItemText from '@material-ui/core/ListItemText';

const drawerWidth = 240;

const useStyles = makeStyles(theme => ({
  root: {
    display: 'flex',
  },
  appBar: {
    width: `calc(100% - ${drawerWidth}px)`,
    marginLeft: drawerWidth,
  },
  drawer: {
    width: drawerWidth,
    flexShrink: 0,
  },
  drawerPaper: {
    width: drawerWidth,
  },
  toolbar: theme.mixins.toolbar,
  content: {
    flexGrow: 1,
    backgroundColor: theme.palette.background.default,
    padding: theme.spacing(3),
  },
}));

export default function PermanentDrawerLeft() {
  const classes = useStyles();

  return (
    <div className={classes.root}>
      <CssBaseline />
      <AppBar position="fixed" className={classes.appBar}>
        <Toolbar>
          <Typography variant="h6" noWrap>
            Portfolio Website
          </Typography>
        </Toolbar>
      </AppBar>
      <Drawer
        className={classes.drawer}
        variant="permanent"
        classes={{
          paper: classes.drawerPaper,
        }}
        anchor="left"
      >
        <div className={classes.toolbar} />
        <Divider />
        <List>
          {['Home', 'About', 'Projects', 'Contact'].map((text, index) => (
            <ListItem button key={text}>
              <ListItemText primary={text} />
            </ListItem>
          ))}
        </List>
      </Drawer>
      <main className={classes.content}>
        <div className={classes.toolbar} />
        <Typography paragraph>
          Welcome to my portfolio website! This site showcases my projects and experiences as a developer.
        </Typography>
      </main>
    </div>
  );
}





## Setup


You will need to install Material-UI by running npm install @material-ui/core. You can then include this code in your React app and deploy it to Github Pages using the steps outlined in the Github Pages documentation.



# elaborate
Here are the steps to set up a Material-UI portfolio website with a side menu using Github Pages:

Create a new Github repository to host your portfolio website.

Set up a local development environment for your React.js app by creating a new directory and running npm init to initialize a new npm project.

Install Material-UI by running npm install @material-ui/core.

Create a new file called index.js and copy the code I provided in my previous answer into this file.

In the terminal, run npm start to start a local development server and see your app in action.

Once you're happy with how your website looks and functions, it's time to deploy it to Github Pages. Create a new branch called gh-pages and push it to your Github repository.

In your Github repository's settings, under the Github Pages section, select the gh-pages branch as the source and save your changes.

Wait a few moments for Github Pages to build your website and then visit the URL provided in the Github Pages section to see your live portfolio website!

That's it! You now have a fully functional Material-UI portfolio website with a side menu hosted on Github Pages. You can continue to build out your site and make updates as needed, and your changes will be automatically reflected on your live website.

