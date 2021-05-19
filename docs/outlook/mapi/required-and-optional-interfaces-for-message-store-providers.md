---
title: Erforderliche und optionale Schnittstellen für Store Anbieter
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
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Erforderliche und optionale Schnittstellen für Store Anbieter

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Schnittstellen, die sich auf Nachrichtenspeicheranbieter beziehen. Aufgrund der vielzahl von Features, die ein Nachrichtenspeicher implementieren kann, sind einige dieser Schnittstellen erforderlich, andere nicht. In der folgenden Tabelle sind die MAPI-Schnittstellen aufgeführt, die mit Nachrichtenspeicheranbietern verknüpft sind, gibt an, ob die Schnittstellen erforderlich oder optional sind, und beschreibt deren Zweck.
  
|**Schnittstelle**|**Status**|**Beschreibung**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Erforderlich  <br/> |Meldet sich an und aus eines Nachrichtenspeichers an.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, überprüft die Identität des Nachrichtenspeichers und verarbeitet Benachrichtigungen.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Erforderlich  <br/> |Öffnet Ordner oder Nachrichten, sucht spezielle Ordner und verarbeitet Nachrichtenübermittlungen.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erforderlich  <br/> |Sucht und bearbeitet Nachrichten und Unterordner.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Erforderlich  <br/> |Bearbeitet Anlagen und legt einige Eigenschaften einer Nachricht fest.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Erforderlich  <br/> |Ermöglicht anderen Objekten das Präsentieren von Datensammlungen für verschiedene MAPI-Komponenten.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Erforderlich  <br/> |Ermöglicht Clients, den Status eines Nachrichtenspeichers zu überprüfen und einige Konfigurationsaufgaben auszuführen.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Optional.  <br/> |Zugrifft auf Nachrichtenanlageneigenschaften, wenn der Speicheranbieter Dateianlagen unterstützt.  <br/> |
|**IStorage** <br/> |Optional.  <br/> |Verwaltet strukturierte Speicherobjekte, wenn der Speicheranbieter OLE-Objektanlagen unterstützt.  <br/> |
|**IStream** <br/> |Optional.  <br/> |Ermöglicht Nachrichten- und Anlagenobjekten das Lesen und Schreiben von Daten in Streamobjekte.  <br/> |
|**IStreamDocfile** <br/> |Optional.  <br/> |Ermöglicht einigen Dienstanbietern das Öffnen eines Speicherobjekts, z. B. einer Zusammengesetztdatei im OLE 2.0-Dateiformat.  <br/> |
   
Die grundlegenden Informationen, die Sie zum Implementieren von **IMAPIFolder,** **IMessage,** **IMAPIStatus** und **IMAPITable** benötigen, sind in den Referenzthemen für diese Schnittstellen dokumentiert. Dieser Abschnitt enthält ergänzende Informationen, die direkter mit Nachrichtenspeicheranbietern in Zusammenhang stehen. Die restlichen MAPI-Schnittstellen sollten gemäß den Informationen in diesem Abschnitt und in den entsprechenden Referenzthemen implementiert werden. Weitere Informationen zum Implementieren von **IStorage,** **IStream** und **IStreamDocFile** finden Sie im Abschnitt COM und ActiveX Object Services im Windows SDK.
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines MAPI-Nachrichtenspeicheranbieters](developing-a-mapi-message-store-provider.md)

