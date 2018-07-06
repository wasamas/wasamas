desc 'setup reverse proxy server'
task :proxy do
	sh 'ansible-playbook proxy.yml'
end

desc 'setup wasamas server'
task :wasamas do
	sh 'ansible-playbook wasamas.yml'
end

desc 'backup database'
task :backup do
	dir = Time.now.strftime('%Y%m%d%H%M%S')
	sh "ssh wasamas.net sudo docker-compose -f /opt/massr/docker-compose.yml exec -T mongodb mongodump -d massr -o /data/db/backup/#{dir}"
	sh "scp -r wasamas.net:/opt/massr/data/db/backup/#{dir} ."
end

task default: [:proxy, :wasamas]
