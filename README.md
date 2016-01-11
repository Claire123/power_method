# power_method
n=3
r=rand(n);
s=r'*r;
s=s/trace(s);
[V,lambda]=eig(s);
 
 v=rand(n,1);
 
 
for i=1:10
    
v_new=s*v;
E=norm(v_new)/norm(v);
v=v_new;

end
v=v/norm(v);
s_new=s-E*v*v';

s_new,v,E
 
