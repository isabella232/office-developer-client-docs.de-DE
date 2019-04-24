---
title: Informationen zum Festlegen der L�sung Reihenfolge f�r Adresslisten in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321833"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Für jedes Profil unterstützt Microsoft Office Outlook mehrere Adresslisten, und Benutzer können die Reihenfolge der Adresslisten angeben, anhand der Empfänger in E-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden. Sie können beispielsweise die Auflösungsreihenfolge so festlegen, dass Namen zuerst anhand des Outlook-Adressbuchs und dann anhand der globalen Adressliste aufgelöst werden. Auf einem Computer ein Benutzer im Adressbuch �ffnen, klicken Sie auf **Extras** und dann auf **Optionen**, um diesen Auftrag L�sung anzugeben. Es ist jedoch in einer Unternehmensumgebung effizienter f�r IT-Administratoren die Reihenfolge der Adresslisten programmgesteuert festgelegt mit dem Namen aufgel�st werden. Diese Art von Code kann als Teil eines Skripts zum Starten Automation verwendet werden, die von ein Administrator innerhalb des Unternehmens bereitgestellt. 
  
MAPI unterstützt die **[SetSearchPath](iaddrbook-getsearchpath.md)**-Methode in der **[IAddrBook](iaddrbookimapiprop.md)**-Schnittstelle, sodass Sie einen neuen Suchpfad in dem Profil festlegen können, der für die Namensauflösung verwendet wird. Um die **IAddrBook::SetSearchPath**-Methode zu verwenden, müssen Sie die gewünschte Auflösungsreihenfolge mithilfe eines Arrays angeben, das Container der relevanten Adressbücher in der Reihenfolge enthält, in der diese aufgelöst werden sollten. Jeder Eintrag in diesem Array sollte auch die Eintrags-ID des entsprechenden Adressbuchs enthalten. 
  
Nachfolgend finden Sie Codebeispiele dafür, wie ein benutzerdefinierter Suchpfad für Adresslisten angegeben wird.
  
- [Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: Ändern der Adressbuch-Sortierreihenfolge mit SetSearchPath](https://support.microsoft.com/kb/292590)
    

