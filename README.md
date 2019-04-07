# 实验三
## UI组件
### ActionMode
#### 截图
![无法显示](/images/1.jpg)
![无法显示](/images/2.jpg)
#### 关键代码
```
 public boolean onActionItemClicked(ActionMode actionMode, MenuItem menuItem) {
                switch (menuItem.getItemId()){
                    case R.id.menu_delete:
                        for(int i=checklist.size()-1;i>=0;i--){
                            if(checklist.get(i)==1){
                                list.remove(i);
                                checklist.remove(i);
                                simpleAdapter.notifyDataSetChanged();
                                actionMode.finish();
                            }
                        }
                        break;
                }
                return true;
            }
```
