void createTree(node *root,string str){	//[LE,RE]
	int bracketL=1,bracketR=0;
	vector<int> balance,left,right;
	int index=1;
	while(bracketL!=bracketR){
		if(str.at(index)=='(')
			bracketL++;
		else if(str.at(index)==')')
			bracketR++;
		else if(str.at(index)!=','){
			if(bracketL==bracketR+1)
				if(root->leftChild==nullptr){
					root->plusLeft();
					root->leftChild->setData(str.at(index));
					//recursion
					string input=str;
					input.erase(input.begin(),input.begin()+index+1);
					createTree(root->leftChild,input);
				}
				else{
					root->plusRight();
					root->rightSibling->setData(str.at(index));
					//recursion
					string input=str;
					input.erase(input.begin(),input.begin()+index+1);
					createTree(root->rightSibling,input);
				}
		}
		index++;
	}
}
