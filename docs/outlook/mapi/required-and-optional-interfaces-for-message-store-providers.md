---
title: Erforderliche und optionale Schnittstellen für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420920"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Erforderliche und optionale Schnittstellen für Nachrichtenspeicher Anbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Gruppe von Schnittstellen, die sich auf Nachrichtenspeicher Anbieter beziehen. Aufgrund der großen Palette von Features, die ein Nachrichtenspeicher für die Implementierung auswählen kann, sind einige dieser Schnittstellen erforderlich, andere nicht. In der folgenden Tabelle sind die MAPI-Schnittstellen aufgelistet, die sich auf Nachrichtenspeicher Anbieter beziehen, gibt an, ob die Schnittstellen erforderlich oder optional sind, und beschreibt deren Zweck.
  
|**Schnittstelle**|**Status**|**Beschreibung**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Erforderlich  <br/> |Meldet ein-und Ausschalten eines Nachrichtenspeichers an.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, überprüft die Identität des Nachrichtenspeichers und verarbeitet Benachrichtigungen.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, sucht nach speziellen Ordnern und verarbeitet Nachrichtenübermittlungen.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erforderlich  <br/> |Sucht und bearbeitet Nachrichten und Unterordner.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Erforderlich  <br/> |Bearbeitet Anlagen und legt einige der Eigenschaften einer Nachricht fest.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Erforderlich  <br/> |Ermöglicht anderen Objekten das darstellen von Datensammlungen für verschiedene MAPI-Komponenten.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Erforderlich  <br/> |Ermöglicht es Clients, den Status eines Nachrichtenspeichers zu überprüfen und einige Konfigurationsaufgaben auszuführen.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Optional  <br/> |Greift auf Eigenschaften der Nachrichtenanlage zu, wenn der Informationsspeicher Anbieterdatei Anlagen unterstützt.  <br/> |
|**IStorage** <br/> |Optional  <br/> |Verwaltet strukturierte Speicherobjekte, wenn der Informationsspeicher Anbieter OLE-Objekt Anlagen unterstützt.  <br/> |
|**IStream** <br/> |Optional  <br/> |Ermöglicht es Message-und Attachment-Objekten, Daten in Stream-Objekte zu lesen und zu schreiben.  <br/> |
|**IStreamDocfile** <br/> |Optional  <br/> |Ermöglicht es einigen Dienstanbietern, ein Speicherobjekt zu öffnen, beispielsweise eine Verbunddatei im OLE 2,0-Dateiformat.  <br/> |
   
Die grundlegenden Informationen, die Sie für die Implementierung von **IMAPIFolder**, **IMessage**, **IMAPIStatus**und **IMAPITable** benötigen, sind in den Referenzthemen zu diesen Schnittstellen dokumentiert. Dieser Abschnitt enthält zusätzliche Informationen, die sich direkt auf Nachrichtenspeicher Anbieter beziehen. Die restlichen MAPI-Schnittstellen sollten gemäß den Informationen in diesem Abschnitt und in den entsprechenden Referenzthemen implementiert werden. Weitere Informationen zum Implementieren von **IStorage**, **IStream**und **ISTREAMDOCFILE**finden Sie im Abschnitt com-und ActiveX-Objektdienste im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

