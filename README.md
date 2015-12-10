# MikroTik-API
API to MikroTik RouterOS

See http://search.cpan.org/~martingo/MikroTik-API/ for documentation

### Quickstart
```perl
use MikroTik::API;
my $api = MikroTik::API->new({
	host => 'mikrotik.example.org',
	username => 'whoami',
	password => 'SECRET',
});
my ( $ret_get_identity, @aoh_identity ) = $api->query( '/system/identity/print', {}, {} );
print "Name of router: $aoh_identity[0]->{name}\n";
```

