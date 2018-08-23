---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ae2729ec5620b6b408a5c999d4b6ede7143bed2f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584565"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Formular in einer Clientanwendung Formular Viewer verwaltet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Kontext-Objekte anzeigen  <br/> |
|Implementiert von:  <br/> |Formular-Viewer  <br/> |
|Aufgerufen von:  <br/> |Formular-Objekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewContext  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Verwaltet ein Formular Registrierung Erhalt von Benachrichtigungen zu Änderungen im Viewer.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Die nächste oder vorherige Nachricht im Formular-Viewer aktiviert.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Ruft die aktuellen Drucken von Informationen.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Ruft einen Datenstrom zum Speichern der aktuellen Nachricht verwendet werden soll.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Ruft den aktuellen Status der Viewer ab.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, in der Ansicht Context-Objekt enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

