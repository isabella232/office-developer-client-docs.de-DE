---
title: Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM
TOCTitle: Registering Business Objects on the Client for Use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f3d29d20200b6e435ffafaaa35c7f507b88b939
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474272"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM


**Betrifft**: Access 2013 | Office 2013

Für benutzerdefinierte Geschäftsobjekte muss sichergestellt werden, dass deren Programmname (ProgId) auf Clientseite einem Bezeichner (CLSID) zugeordnet werden kann, der über DCOM verwendet werden kann. Deshalb muss die ProgID des DCOM-Objekts in der Registrierung auf Clientseite vorhanden und der Klassen-ID des serverseitigen Geschäftsobjekts zugeordnet sein. Für die anderen unterstützten Protokolle (HTTP, HTTPS und In-Process) ist dies nicht erforderlich.

Wenn Sie z. B. eine Geschäftsobjekt des Servers namens MyBObj mit einer bestimmten Klassen-ID, z. B. "{00112233-4455-6677-8899-00AABBCCDDEE}", verfügbar machen, müssen folgende Einträge der Clientregistrierung hinzugefügt werden:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

