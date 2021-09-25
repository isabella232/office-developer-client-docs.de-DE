---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e95a52056f8ad9936e8071176fc2bd55e16acfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587916"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Formularanzeigen die Verarbeitung des Speichers eines Formulars und den Übergang zwischen den verschiedenen Zuständen.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Speichern von Nachrichtenobjekten  <br/> |
|Implementiert von:  <br/> |Formularobjekte  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IPersistMessage  <br/> |
|Zeigertyp:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](ipersistmessage-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler im Formularobjekt enthält.  <br/> |
|[Getclassid](ipersistmessage-getclassid.md) <br/> |Gibt einen Bezeichner zurück, der den Formularserver darstellt, der das Formular verwalten kann.  <br/> |
|[Isdirty](ipersistmessage-isdirty.md) <br/> |Überprüft das Formular auf Änderungen, die seit dem letzten Speichern vorgenommen wurden.  <br/> |
|[Initnew](ipersistmessage-initnew.md) <br/> |Initialisiert eine neue Nachricht.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Lädt das Formular für eine angegebene Nachricht.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Speichert ein überarbeitetes Formular wieder in der Nachricht, aus der es geladen oder erstellt wurde.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Benachrichtigt das Formular, dass ein Speichervorgang abgeschlossen wurde.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Bewirkt, dass das Formular seine aktuelle Nachricht freigibt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Alle Formulare sind erforderlich, um die **IPersistMessage-Schnittstelle** zu implementieren. 
  
 **IPersistMessage** funktioniert ähnlich wie die OLE [IPersistStorage-Schnittstelle.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) Weitere Informationen finden Sie unter den **IPersistStorage-Methoden.** 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

