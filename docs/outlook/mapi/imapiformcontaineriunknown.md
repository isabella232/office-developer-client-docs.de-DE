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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407529"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Formulare in Formularbibliotheken. Diese Schnittstelle wird zum Erstellen anwendungsspezifischer Formularbibliotheken verwendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularcontainerobjekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Formularbibliotheken  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installiert ein Formular in einem Formularcontainer.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Entfernt ein bestimmtes Formular aus einem Formularcontainer.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften zurück, die von allen in einem Formularcontainer installierten Formularen verwendet werden.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Gibt den Anzeigenamen eines Formularcontainers zurück.  <br/> |
|[GetLastError](imapiformcontainer-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formularcontainerobjekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

