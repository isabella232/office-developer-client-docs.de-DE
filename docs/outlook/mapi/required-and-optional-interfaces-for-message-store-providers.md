---
title: Erforderliche und optionale Schnittstellen Nachrichtenspeicheranbieter
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 3305aaadbcf7d53b801ddaf7e31a0d63145fc7ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586963"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Erforderliche und optionale Schnittstellen Nachrichtenspeicheranbieter

 
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI definiert eine Reihe von Schnittstellen, die Nachricht Speicher-Anbieter beziehen. Aufgrund der Vielzahl von Features, die zum Implementieren ein Nachrichtenspeichers auswählen können, sind einige dieser Schnittstellen erforderlich und sind nicht. Die folgende Tabelle listet die MAPI-Schnittstellen, die im Zusammenhang mit der Nachricht-Anbieter, gibt an, ob die Schnittstellen sind erforderlich oder optional und beschreibt deren Zweck.
  
|**Schnittstelle**|**Status**|**Beschreibung**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Erforderlich  <br/> |Protokolle an und von einem Nachrichtenspeicher.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Erforderlich  <br/> |Ordner oder Nachrichten öffnet, überprüft die Nachrichtenspeicher Identität und Benachrichtigungen behandelt.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Erforderlich  <br/> |Ordner oder Nachrichten öffnet, sucht nach Spezialordner und Nachrichtenübermittlungen behandelt.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Erforderlich  <br/> |Sucht und Nachrichten und Unterordner bearbeitet.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Erforderlich  <br/> |Anlagen bearbeitet und einige der Eigenschaften einer Nachricht festgelegt.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Erforderlich  <br/> |Ermöglicht es anderen Objekten Sammlungen von Daten zu verschiedenen MAPI-Komponenten durchzuführen.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Erforderlich  <br/> |Ermöglicht es Clients, um den Status eines Nachrichtenspeichers überprüfen und einige Konfigurationsaufgaben ausführen.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Optional  <br/> |Zugriffe Nachrichteneigenschaften Anlage Wenn Speicheranbieter Dateianlagen unterstützt.  <br/> |
|**IStorage** <br/> |Optional  <br/> |Strukturierte Speicherobjekte verwaltet, wenn Speicheranbieter OLE-Objekt von Anlagen unterstützt.  <br/> |
|**IStream** <br/> |Optional  <br/> |Können Nachrichten und Anlagen Objekte zum Lesen und Schreiben von Daten in Stream-Objekten.  <br/> |
|**IStreamDocfile** <br/> |Optional  <br/> |Einige Dienstanbieter ein Speicherobjekt, wie etwa eine Verbunddatei im OLE 2.0-Dateiformat öffnen können.  <br/> |
   
Die grundlegende Informationen zum Implementieren von **IMAPIFolder**, **IMessage**, **IMAPIStatus**und **IMAPITable** benötigten ist in den Referenzthemen für diese Schnittstellen dokumentiert. Dieser Abschnitt enthält zusätzliche Informationen, die direkt Nachricht Anbieter verknüpft ist. Entsprechend den Informationen in diesem Abschnitt und in den entsprechenden Referenzthemen sollte der Rest der MAPI-Schnittstellen implementiert werden. Siehe Abschnitt COM und ActiveX-Objektdienste im Windows SDK für Weitere Informationen zum Implementieren von **IStorage** **IStream**und **IStreamDocFile**.
  
## <a name="see-also"></a>Siehe auch



[Entwickeln eines Providers MAPI-Nachrichtenspeicher](developing-a-mapi-message-store-provider.md)

