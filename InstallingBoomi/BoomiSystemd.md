[Unit]
Description= Boomi Atom
RequiresMountsFor=/home/jdaris
Wants=network-online.target
After=network.target network-online.target
[Service]
Type=forking
Restart=always
User=jdaris
ExecStart=/bin/sh -c "/home/jdaris/Boomi_AtomSphere/Atom/Atom_Boomi_Atom_Temp_JD_Dev/bin/atom start"
ExecStop=/bin/sh -c "/home/jdaris/Boomi_AtomSphere/Atom/Atom_Boomi_Atom_Temp_JD_Dev/bin/atom stop"
ExecReload=/bin/sh -c "/home/jdaris/Boomi_AtomSphere/Atom/Atom_Boomi_Atom_Temp_JD_Dev/bin/atom restart"
[Install]
WantedBy=multi-user.target
