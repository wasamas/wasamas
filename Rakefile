desc 'setup reverse proxy server'
task :proxy do
	sh 'ansible-playbook proxy.yml'
end

desc 'setup wasamas server'
task :wasamas do
	sh 'ansible-playbook wasamas.yml'
end

task default: [:proxy, :wasamas]
