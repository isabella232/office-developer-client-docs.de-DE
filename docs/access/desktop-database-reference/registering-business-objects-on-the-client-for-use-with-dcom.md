---
title: Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a63a2af1a5cadd112cfc1f75471247c7481115b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557876"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a>Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM

**Gilt für**: Access 2013, Office 2013

Für benutzerdefinierte Geschäftsobjekte muss sichergestellt werden, dass deren Programmname (ProgId) auf Clientseite einem Bezeichner (CLSID) zugeordnet werden kann, der über DCOM verwendet werden kann. Deshalb muss die ProgID des DCOM-Objekts in der Registrierung auf Clientseite vorhanden und der Klassen-ID des serverseitigen Geschäftsobjekts zugeordnet sein. Für die anderen unterstützten Protokolle (HTTP, HTTPS und In-Process) ist dies nicht erforderlich.

For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

