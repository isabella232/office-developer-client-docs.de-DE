---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9bc9fed3cb1a960eb0875dd4efefad3eb632116d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600841"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet ein Formular in der Formularanzeige einer Clientanwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Anzeigen von Kontextobjekten  <br/> |
|Implementiert von:  <br/> |Formularanzeigen  <br/> |
|Aufgerufen von:  <br/> |Formularobjekte  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIViewContext  <br/> |
|Zeigertyp:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Verwaltet die Registrierung eines Formulars, um Benachrichtigungen über Änderungen im Viewer zu erhalten.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Aktiviert die nächste oder vorherige Nachricht in der Formularanzeige.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Ruft aktuelle Druckinformationen ab.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Ruft einen Datenstrom ab, der zum Speichern der aktuellen Nachricht verwendet werden soll.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Ruft den aktuellen Anzeigestatus ab.  <br/> |
|[Getlasterror](imapiviewcontext-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der im Ansichtskontextobjekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

