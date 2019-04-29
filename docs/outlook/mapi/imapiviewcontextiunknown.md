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
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406031"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet ein Formular im Formular-Viewer einer Clientanwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anzeigen von Kontextobjekten  <br/> |
|Implementiert von:  <br/> |Formular Betrachter  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewContext  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Verwaltet die Registrierung eines Formulars, um Benachrichtigungen zu Änderungen im Viewer zu erhalten.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Aktiviert die nächste oder vorherige Nachricht im Formular-Viewer.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Ruft aktuelle Druckinformationen ab.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Ruft einen Stream ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Ruft den aktuellen viewerstatus ab.  <br/> |
|[Getlasterroraufzurufen](imapiviewcontext-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen über den vorherigen Fehler enthält, der im View-Kontextobjekt auftritt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

