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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309604"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Formularanzeigen die Verarbeitung des Speichers eines Formulars und den Übergang zwischen den verschiedenen Zuständen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Beibehalten von Nachrichtenobjekten  <br/> |
|Implementiert von:  <br/> |Formularobjekte  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPersistMessage  <br/> |
|Zeigertyp:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler im Formularobjekt enthält.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Initialisiert eine neue Nachricht.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Lädt das Formular für eine angegebene Nachricht.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Speichert ein überarbeitetes Formular in der Nachricht zurück, aus der es geladen oder erstellt wurde.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Bewirkt, dass das Formular seine aktuelle Nachricht veröffentlicht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Alle Formulare sind erforderlich, um die **IPersistMessage-Schnittstelle zu** implementieren. 
  
 **IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage-Schnittstelle.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) Weitere Informationen finden Sie unter **IPersistStorage-Methoden.** 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

