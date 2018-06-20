---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792076"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl: IUnknown

  
  
**Betrifft**: Outlook 
  
Aktiviert und ein Button-Steuerelement deaktiviert und führt Aufgaben aus, wenn ein Benutzer von einer Clientanwendung aktivierte Steuerelement klickt. Dienstanbieter implementieren Control-Objekte zum Erstellen von benutzerdefinierter Schaltflächen auf Dialogfelder wie Konfiguration Property Sheets, die mithilfe der Anzeige Tabellen definiert sind. 
  
Weitere Informationen zum Arbeiten mit Tabellen anzeigen und Objekte zu steuern finden Sie unter [Tabellen angezeigt](display-tables.md).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Control-Objekte  <br/> |
|Implementiert von:  <br/> |Dienstanbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIControl  <br/> |
|Zeigertyp:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Schaltfläche-Steuerelement enthält.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Führt eine Aufgabe wie etwa Anzeigen eines Dialogfelds oder einen programmgesteuerten Vorgang starten, wenn Benutzer eine Clientanwendung das Button-Steuerelement klickt.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Ruft einen Wert, der angibt, ob das Schaltflächensteuerelement aktiviert oder deaktiviert ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

