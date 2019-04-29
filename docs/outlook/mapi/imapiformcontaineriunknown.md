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
  
Verwaltet Formulare in Formularbibliotheken. Diese Schnittstelle wird verwendet, um anwendungsspezifische Formularbibliotheken zu erstellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular Containerobjekte  <br/> |
|Implementiert von:  <br/> |Formular Bibliotheks Anbieter  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installiert ein Formular in einem Formular Container.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Entfernt ein bestimmtes Formular aus einem Formular Container.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in Ihrem Formular in einem Formular Container auf und gibt ein Formular Informationsobjekt für dieses Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Löst eine Gruppe von Nachrichtenklassen in Ihre Formulare in einem Formular Container auf und gibt ein Array von Formular Informationsobjekten für diese Formulare zurück.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften zurück, die von allen in einem Formular Container installierten Formularen verwendet werden.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Gibt den Anzeigenamen eines Formular Containers zurück.  <br/> |
|[Getlasterroraufzurufen](imapiformcontainer-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen über den vorherigen Fehler im Formular Containerobjekt enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

