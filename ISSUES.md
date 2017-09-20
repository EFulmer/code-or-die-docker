    psql -h db -p 5432 -U postgres -d "code-or-die" <<( "/code-or-die/code-or-die/bitemporal.sh" "code-or-die" )
    psql: could not connect to server: No such file or directory
       Is the server running locally and accepting
    connections on Unix domain socket "/var/run/postgresql/.s.PGSQL.5432"?
    Traceback (most recent call last):
      File "/usr/local/bin/jinja2", line 11, in <module>
        sys.exit(main())
      File "/usr/local/lib/python3.6/site-packages/jinja2cli/cli.py", line 335, in main
        sys.exit(cli(opts, args))
      File "/usr/local/lib/python3.6/site-packages/jinja2cli/cli.py", line 257, in cli
        output = render(template_path, data, extensions, opts.strict)
      File "/usr/local/lib/python3.6/site-packages/jinja2cli/cli.py", line 183, in render
        output = env.get_template(os.path.basename(template_path)).render(data)
      File "/usr/local/lib/python3.6/site-packages/jinja2/asyncsupport.py", line 76, in render
        return original_render(self, *args, **kwargs)
      File "/usr/local/lib/python3.6/site-packages/jinja2/environment.py", line 1008, in render
        return self.environment.handle_exception(exc_info, True)
      File "/usr/local/lib/python3.6/site-packages/jinja2/environment.py", line 780, in handle_exception
        reraise(exc_type, exc_value, tb)
      File "/usr/local/lib/python3.6/site-packages/jinja2/_compat.py", line 37, in reraise
        raise value.with_traceback(tb)
      File "/code-or-die/code-or-die/bitemporal.sql.template", line 18, in top-level template code
        {% for table in tables %}
    TypeError: 'NoneType' object is not iterable
