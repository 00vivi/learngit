##��װ��git�󣬵�һ�����ã�
	git config --global user.name = "lecion"
	git config --global user.email = "ylc931116@gmail.com"

#��ʼ��һ��Repository
	mkdir rep
	cd rep	
	git init

#add��commit
	git add ***
	git commit -m "***"

#log
	git log --pretty=oneline
	git log --graph --pretty=online --abbrev-commit
	git reflog

#�ص���ʷ�汾
	git reset --hard HEAD^ //HEAD��ʾ��ǰ�汾��HEAD^ ��һ���汾 HEAD^^ �������汾 HEAD~100 ǰ100���汾

#diff �鿴����
	git diff ***

#��������Working Directory��
>�������ܿ�����Ŀ¼ �����紴����learngit�ļ��о���һ��`������`��
#�汾�⣨Repository��
>��������һ������Ŀ¼`.git`��������㹤����������Git�汾�⡣Git�İ汾������˺ܶණ��������Ҫ�ĳ�Ϊ`stage`��`�ݴ���`��git add ������ݾ��Ƿ����ݴ�����ֱ����commit

#�����޸�
	git checkout -- *** //��***�ڹ��������޸�ȫ������
*	û��git add����ָ����Ͱ汾��һģһ��
*	���git add����ָ�����������״̬

#������������unstage��
	git reset HEAD *** //��***���޸Ĵӻ������Ƴ�

#ɾ���ļ�
	rm test.txt
	git rm test.txt
	git commit -m "del test.txt"
>���ɾ���ˣ���git checkout -- test.txt ���ɽ��汾���test.txt�ָ�����������������ɾ�������޸Ķ����Բ��ô˲���

#Զ�ֿ̲�
*	ʹ��Git������SSH Key

		ssh-keygen -t rsa -C "ylc931116@gmail.com"
*	��½Github�� ��Account Settings�� "SSH Keys"ҳ�棬����	id_rsa.pub�������
*	Github�ϴ���Repository `learngit`
*	���������вֿ��git����

		git remote add origin git@github.com:lecion/learngit.git
		git push -u origin master
	>��Ϊ�ǵ�һ���ύ����Ҫ��`-u`�������ѱ���master��֧�������͵�Զ���µ�master��֧�����ѱ��ص�master��֧��Զ��master��֧�����������Ժ��ύ�Ϳɼ�����
*	����Ժ󱾵������޸ģ��Ϳ���ͨ�����������ύ

		git push orgin master

#��õķ�ʽ
>��Զ�̽���һ��Repository�󣬴�Զ��clone
	
	git clone git@github.com:lecion/gitskills.git
#�����·�֧
	git checkout -b dev
>`-b`��ʾ�������л�

	git branch dev
>���ַ�ʽҲ����

#�鿴��֧
	git branch
>���г����з�֧���ڵ�ǰ��֧ǰ��`*`��ע

#�л���֧
	git checkout master
#�ϲ���֧
	git merge dev
#ɾ����֧
	git branch -d dev
	git branch -D dev
>`-D`ǿ��ɾ��û�кϲ��ķ�֧

#�޸�Bug
	git stash
>�ݴ浱ǰ��������������bug�󣬻ص��÷�֧

	git stash list
>�鿴�ݴ��б�

	git stash pop
>���������stash
	
	git stash apply
	git stash drop
	git stash apply@{0}

#�鿴Զ�̿�
	git remote -v
>`-v`��ʾ��ϸ��Ϣ

#���ͷ�֧
	git push origin master
	git push origin dev
*	master��֧������֧�����Ҫʱ����Զ��ͬ����
*	dev��֧�ǿ�����֧���Ŷ����г�Ա����Ҫ�����湤��������Ҳ��Ҫ��Զ��ͬ	����
*	bug��ֻ֧�����ڱ����޸�bug����û��Ҫ�Ƶ�Զ���ˣ������ϰ�Ҫ������ÿ	�ܵ����޸��˼���bug��
*	feature��֧�Ƿ��Ƶ�Զ�̣�ȡ�������Ƿ�����С�����������濪����

#ʹ�ñ�ǩ
	git tag v1.0
	git tag -a v0.9 -m "version 0.9 released" 234234
	git show v0.1
	git tag -d v1.0
	git push origin v1.0
	git push origin --tag
	git push origin:refs/tags/v1.0

