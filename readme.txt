python manage.py db
����
ConfigParser.NoSectionError: No section: 'alembic'
��Ϊ��û��python manage.py db init��ʼ�����ݿ�


python manage.py db init
����alembic.util.CommandError: Directory migrations already exists����
����Ϊ��ǰ������migrations�ļ�Ŀ¼


# �ص�������ʹ��ָ���ı�ʶ�������û�
@login_manager.user_loader

==================================
python hello.py shell
from hello import db
db.drop_all()
db.create_all()

from hello import Role, User

��ɾ��sqlite�ļ��ٽ��������������Ȼ�����ɹ�
python hello.py db init
#Ǩ��
python manage.py db migrate -m "initial migration"
python manage.py db upgrade
# ��ʱ���ֲ�����������������Ҫ�ع�����һ���汾զ���أ����������ҽ��������
python hello.py db downgrade d303dfaaefba��������12Ϊ�������ϴε����ݰ汾


u = User(email='john@example.com', username='john', password='cat')
db.session.add(u)
db.session.commit()