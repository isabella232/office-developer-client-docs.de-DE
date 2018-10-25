---
title: Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391409"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Informationen zum Festlegen der Auflösungsreihenfolge für Adresslisten in Outlook

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Für jedes Profil unterstützt Microsoft Office Outlook mehrere Adresslisten, und Benutzer können die Reihenfolge der Adresslisten angeben, anhand der Empfänger in E-Mail-Nachrichten und Teilnehmer in Besprechungsanfragen aufgelöst werden. Sie können beispielsweise die Auflösungsreihenfolge so festlegen, dass Namen zuerst anhand des Outlook-Adressbuchs und dann anhand der globalen Adressliste aufgelöst werden. Auf einem Computer kann ein Benutzer das Adressbuch öffnen, und dann auf **Extras** und **Optionen** klicken, um die Auflösungsreihenfolge anzugeben. In einer Unternehmensumgebung ist es für IT-Administratoren jedoch effizienter, die Reihenfolge von Adresslisten, anhand der Namen aufgelöst werden, programmgesteuert festzulegen. Diese Art von Code kann als Teil eines Skripts zum Starten Automation verwendet werden, die von ein Administrator innerhalb des Unternehmens bereitgestellt. 
  
MAPI unterstützt die **[SetSearchPath](iaddrbook-getsearchpath.md)**-Methode in der **[IAddrBook](iaddrbookimapiprop.md)**-Schnittstelle, sodass Sie einen neuen Suchpfad in dem Profil festlegen können, der für die Namensauflösung verwendet wird. Um die **IAddrBook::SetSearchPath**-Methode zu verwenden, müssen Sie die gewünschte Auflösungsreihenfolge mithilfe eines Arrays angeben, das Container der relevanten Adressbücher in der Reihenfolge enthält, in der diese aufgelöst werden sollten. Jeder Eintrag in diesem Array sollte auch die Eintrags-ID des entsprechenden Adressbuchs enthalten. 
  
Nachfolgend finden Sie Codebeispiele dafür, wie ein benutzerdefinierter Suchpfad für Adresslisten angegeben wird.
  
- [Programmgesteuertes Festlegen der Auflösungsreihenfolge für Adresslisten](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: Ändern der Adressbuch-Sortierreihenfolge mit SetSearchPath](https://support.microsoft.com/kb/292590)
    

