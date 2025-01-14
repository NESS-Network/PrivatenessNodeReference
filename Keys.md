Node Key File
=============

<node-url>.key.json
-------------------

### filedata
  - vendor
    - Privateness

  - type
    - key

  - for
    - node


### keys
  - private
  - public
  - verify


### url

### nonce
  - cryptographic salt


### master-user
  - master user (admin) name


### tags
  - coma,separated,tags


### tariff
  - amount of coin hours per each tick count


### worm
  - <worm>


directory
---------

### flashdrive

User Key File (flashdrive)
==========================

<username>.key.json
-------------------

### filedata
  - vendor
    - Privateness

  - type
    - key

  - for
    - user


### username

### keys
  - private
    - [array of keys]

  - public
    - [array of keys]

  - verify
    - [array of keys]

  - current
    - current key index (private, public, verify)


### nonce
  - cryptographic salt


### tags
  - coma,separated,tags


### worm
  - <worm>


directory
---------

### flashdrive

Nodes list (local)
==================

nodes.json
----------

### filedata
  - vendor
    - Privateness

  - type
    - data

  - for
    - nodes-list


### nodes[]
  - node_name
    - url
      - service node url where file is stored

    - pub
      - public key

    - ver
      - verify key

    - nonce
    - master
    - tariff
    - tags[]

  - node_name
  - ...


directory
---------

### ~/.privateness-keys

User Key File (local)
=====================

<username>.local.key.json
-------------------------

### filedata
  - vendor
    - Privateness

  - type
    - key

  - for
    - user-local


### username

### keys
  - public
  - private
  - verify


### nonce
  - cryptographic salt


directory
---------

### ~/.privateness-keys

+++
===
+++
===
___
===
Password Encrypted Key File
===========================

<username>.encrypted.keys.json OR <node-url>.encrypted.key.json OR local.encrypted.keys.json
--------------------------------------------------------------------------------------------

### filedata
  - vendor
    - Privateness

  - type
    - encrypted-keys

  - for
    - user
    - node
    - local

  - cipher
    - salsa20


### keys [...]
  - Password Encrypted Key 1 gwh8gw47gh8o
  - Password Encrypted Key 2 wo3hgw78o3hgw
  - ...


### crc [...]
  - crc for key 0
  - crc for key 1
  - ........


directory
---------

### flashdrive

Files info (local)
==================

files.json
----------

### filedata
  - vendor
    - Privateness

  - type
    - service

  - for
    - files


### files
  - node url (service node URL where file is stored)
    - shadowname
      - filename
      - cipher
        - 78oqf3hfyuf;ohf9qp43hgafgre (separate cipher for each file)

      - cipher-type
        - salsa20

      - status
        - c created
        - e encryptiong
        - u uploading
        - n on service node
        - w downloading
        - d decrypting

      - paused
        - current processing is paused or not

      - directory
        - directory ID
          - Directory ID from directories.json

      - source
        - Full source file path

    - ...


directory
---------

### ~/.privateness-keys

My Nodes (local)
================

directory
---------

### ~/.privateness-keys


my-nodes.json
-------------

### filedata
  - vendor
    - Privateness

  - type
    - service

  - for
    - node


### current-node
  - node URL


### my-nodes
  - node_name
    - shadowname
      - users shadowname (for this current node)

  - node_name
  - node_name

Blockchain RPC (local)
======================

blockchain-rpc.json
-------------------

### filedata
  - vendor
    - Privateness

  - type
    - config

  - for
    - blockchain


### rpc-host

### rpc-port

### rpc-user

### rpc-password

Directories (local)
===================

directory
---------

### ~/.privateness-keys


directories.json
----------------

### filedata
  - vendor
    - Privateness

  - type
    - service

  - for
    - files-directories


### directories
  - node url (service node URL where file is stored)
    - id
      - name
      - parent
        - parent ID

    - ...


### current
  - node url
    - Current directory ID (default 0)

  - ...


Tasks
-----

