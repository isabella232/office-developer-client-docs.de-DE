---
title: Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM
TOCTitle: Registering business objects on the client for use with DCOM
ms:assetid: f98c419f-a8c0-b087-bb98-ab760154e99b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250269(v=office.15)
ms:contentKeyID: 48548818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7479eefcc975ca0fe7bb7fe0d51796d1b1f416b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307085"
---
# <a name="registering-business-objects-on-the-client-for-use-with-dcom"></a><span data-ttu-id="de38c-102">Registrieren von Geschäftsobjekten auf dem Client für die Verwendung mit DCOM</span><span class="sxs-lookup"><span data-stu-id="de38c-102">Registering business objects on the client for use with DCOM</span></span>

<span data-ttu-id="de38c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de38c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de38c-p101">Für benutzerdefinierte Geschäftsobjekte muss sichergestellt werden, dass deren Programmname (ProgId) auf Clientseite einem Bezeichner (CLSID) zugeordnet werden kann, der über DCOM verwendet werden kann. Deshalb muss die ProgID des DCOM-Objekts in der Registrierung auf Clientseite vorhanden und der Klassen-ID des serverseitigen Geschäftsobjekts zugeordnet sein. Für die anderen unterstützten Protokolle (HTTP, HTTPS und In-Process) ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de38c-p101">Custom business objects need to ensure that the client side can map their program name (ProgId) to an identifier (CLSID) that can be used over DCOM. For this reason, the ProgID of the DCOM object must be in the client-side registry and map to the class ID of the server-side business object. For the other supported protocols (HTTP, HTTPS, and in-process), this is not necessary.</span></span>

<span data-ttu-id="de38c-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span><span class="sxs-lookup"><span data-stu-id="de38c-107">For example, if you expose a server-side business object called MyBObj with a specific class ID, for instance, "{00112233-4455-6677-8899-00AABBCCDDEE}", make sure that the following entries are added to the client-side registry:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT] 
\MyBObj 
 \Clsid 
 (Default) "{00112233-4455-6677-8899-00AABBCCDDEE}" 
```

