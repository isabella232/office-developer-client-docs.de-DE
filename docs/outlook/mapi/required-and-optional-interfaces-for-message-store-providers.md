---
title: Erforderliche und optionale Schnittstellen für Nachrichtenanbieter Store
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 15937321d1f082f93413f541daa40e7bdb4e8f80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578809"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Erforderliche und optionale Schnittstellen für Nachrichtenanbieter Store

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Schnittstellen, die sich auf Nachrichtenspeicheranbieter beziehen. Aufgrund der vielzahl von Features, die ein Nachrichtenspeicher implementieren kann, sind einige dieser Schnittstellen erforderlich, andere nicht. In der folgenden Tabelle sind die MAPI-Schnittstellen aufgeführt, die sich auf Nachrichtenspeicheranbieter beziehen, gibt an, ob die Schnittstellen erforderlich oder optional sind, und beschreibt deren Zweck.
  
|**Schnittstelle**|**Status**|**Beschreibung**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Erforderlich  <br/> |Meldet sich bei einem Nachrichtenspeicher an und von diesem ab.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, überprüft die Identität des Nachrichtenspeichers und verarbeitet Benachrichtigungen.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, sucht nach speziellen Ordnern und verarbeitet Nachrichtenübermittlungen.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erforderlich  <br/> |Sucht und bearbeitet Nachrichten und Unterordner.  <br/> |
|[Imessage](imessageimapiprop.md) <br/> |Erforderlich  <br/> |Bearbeitet Anlagen und legt einige Eigenschaften einer Nachricht fest.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Erforderlich  <br/> |Ermöglicht anderen Objekten, Sammlungen von Daten für verschiedene MAPI-Komponenten darzustellen.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Erforderlich  <br/> |Ermöglicht Clients, den Status eines Nachrichtenspeichers zu überprüfen und einige Konfigurationsaufgaben auszuführen.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Optional  <br/> |Greift auf Nachrichtenanlageneigenschaften zu, wenn der Speicheranbieter Dateianlagen unterstützt.  <br/> |
|**IStorage** <br/> |Optional  <br/> |Verwaltet strukturierte Speicherobjekte, wenn der Speicheranbieter OLE-Objektanlagen unterstützt.  <br/> |
|**IStream** <br/> |Optional  <br/> |Ermöglicht Nachrichten- und Anlagenobjekten das Lesen und Schreiben von Daten zum Streamen von Objekten.  <br/> |
|**IStreamDocfile** <br/> |Optional  <br/> |Ermöglicht einigen Dienstanbietern das Öffnen eines Speicherobjekts, z. B. einer Verbunddatei im OLE 2.0-Dateiformat.  <br/> |
   
Die grundlegenden Informationen, die Sie zum Implementieren von **IMAPIFolder**, **IMessage**, **IMAPIStatus** und **IMAPITable** benötigen, sind in den Referenzthemen für diese Schnittstellen dokumentiert. Dieser Abschnitt enthält ergänzende Informationen, die sich direkter auf Nachrichtenspeicheranbieter beziehen. Die restlichen MAPI-Schnittstellen sollten gemäß den Informationen in diesem Abschnitt und in den entsprechenden Referenzthemen implementiert werden. Weitere Informationen zum Implementieren von **IStorage,** **IStream** und **IStreamDocFile** finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

