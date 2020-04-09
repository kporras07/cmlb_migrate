Content Migration to Layout Builder
===================================

This module intends to be a PoC for Content Migration to Layout Builder.

# Components

## Migrate group config
Simple migrate group config file

## Migrate file
Migrate file that takes body field and separate into multiple components using a callback.

## Callback (in .module file)
This callback takes the body field and looking for specific tags, separate them into different block_content entities.
Then, it adds those block_content entities to single layout builder section as components.

# Improvements needed

- The callback probably should be a process plugin
- The callback (or process plugin) should be able to keep the order of the original body.
Example: some text, custom tag, some text, custom tag. Right now, it will be: some text, some text, custom tag, custom tag.