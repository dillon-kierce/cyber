<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dillon Kierce Terminal</title>
    <script src="https://cdn.jsdelivr.net/npm/jquery"></script>
    <script src="https://cdn.jsdelivr.net/npm/jquery.terminal/js/jquery.terminal.min.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/jquery.terminal/css/jquery.terminal.min.css"/>
    <style>
        body {
            margin: 0;
            height: 100vh;
            background-color: black;
            color: #33ff33;
            font-family: monospace;
        }
    </style>
</head>
<body>
    <script>
        $(function() {
            $('body').terminal({
                hello: function(name) {
                    this.echo('Hello, ' + name + '! Welcome to Dillon Kierce\'s Terminal Webpage.');
                },
                about: function() {
                    this.echo("Dillon Kierce is a cybersecurity specialist, researcher, and educator.");
                },
                projects: function() {
                    this.echo("- Cybersecurity Research\n- Teaching @ University\n- Blockchain Security\n- Honeypot Monitoring");
                },
                contact: function() {
                    this.echo("Email: dillon@example.com\nGitHub: github.com/dillon-kierce\nTwitter: @dillonkierce");
                },
                cat: function(width = 408, height = 287) {
                    this.echo('<img src="https://placekitten.com/' + width + '/' + height + '">', {raw: true});
                },
                help: function() {
                    this.echo("Available commands: hello [name], about, projects, contact, cat [width] [height], help");
                }
            }, {
                greetings: `
 _______  __   __  _______  _______  ___      ___   __   __  _______
|       ||  |_|  ||       ||       ||   |    |   | |  | |  ||       |
|   _   ||       ||    ___||   _   ||   |    |   | |  |_|  ||    ___|
|  | |  ||       ||   |___ |  | |  ||   |    |   | |       ||   |___ 
|  |_|  ||       ||    ___||  |_|  ||   |___ |   | |       ||    ___|
|       || ||_|| ||   |___ |       ||       ||   | |   _   ||   |___ 
|_______||_|   |_||_______||_______||_______||___| |__| |__||_______|

Type 'help' to see available commands.
                `
            });
        });
    </script>
</body>
</html>
