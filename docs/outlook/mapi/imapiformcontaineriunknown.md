---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792154"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer: IUnknown

  
  
**Betrifft**: Outlook 
  
Formulare in Formularbibliotheken verwaltet. Diese Schnittstelle wird verwendet, um anwendungsspezifische Formularbibliotheken erstellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular Container-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter für Formular-Bibliothek  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installiert ein Formular in einem Formular-Container.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Entfernt ein bestimmtes Formular aus einem Formular Container.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in seiner Form in einem Formular Container und ein Formular Informationen-Objekt für dieses Formular zurückgegeben.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Eine Gruppe von Nachrichtenklassen in Formularen in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften verwendet, die für alle Formen in einem Formular Container installiert.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Gibt den Anzeigenamen eines Containers Formular zurück.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur mit Informationen über den vorherigen Fehler auftritt, auf das Formular Container-Objekt zurück.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

