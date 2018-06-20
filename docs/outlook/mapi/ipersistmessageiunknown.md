---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792764"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage: IUnknown

  
  
**Betrifft**: Outlook 
  
Ermöglicht das Formular Leser von Berichten, die Speicherung eines Formulars und zum Wechseln zwischen den verschiedenen Zuständen zu behandeln.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Beibehalten von Message-Objekten  <br/> |
|Implementiert von:  <br/> |Formular-Objekte  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPersistMessage  <br/> |
|Zeigertyp:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu den vorherigen Fehler in das Form-Objekt enthält, zurück.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Gibt einen Bezeichner, der den Formular Server darstellt, der das Formular verwaltet werden können.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Überprüft das Formular, damit die Änderungen, die seit dem letzten Speichervorgang vorgenommen wurden.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialisiert eine neue Nachricht an.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Lädt das Formular für eine angegebene Nachricht.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Speichert eine überarbeitete Formular an die Nachricht aus der es geladen oder erstellt wurde.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Das Formular benachrichtigt, einen Vorgang abgeschlossen wurde.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Bewirkt, dass das Formular, um die aktuelle Nachricht freigeben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Alle Formulare sind erforderlich, um die **IPersistMessage** -Schnittstelle implementieren. 
  
 **IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) -Schnittstelle. Weitere Informationen finden Sie unter die **IPersistStorage** -Methoden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

