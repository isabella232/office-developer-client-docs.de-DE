---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7691cdaf21ae98b963aa63e0af7ab2c151a4f3da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576023"
---
# <a name="imapiformcontainer--iunknown"></a>IMAPIFormContainer : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwaltet Formulare in Formularbibliotheken. Diese Schnittstelle wird verwendet, um anwendungsspezifische Formularbibliotheken zu erstellen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularcontainerobjekte  <br/> |
|Implementiert von:  <br/> |Formularbibliotheksanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormContainer  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMCONTAINER  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[InstallForm](imapiformcontainer-installform.md) <br/> |Installiert ein Formular in einem Formularcontainer.  <br/> |
|[RemoveForm](imapiformcontainer-removeform.md) <br/> |Entfernt ein bestimmtes Formular aus einem Formularcontainer.  <br/> |
|[ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in ihrem Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.  <br/> |
|[CalcFormPropSet](imapiformcontainer-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften zurück, die von allen in einem Formularcontainer installierten Formularen verwendet werden.  <br/> |
|[GetDisplay](imapiformcontainer-getdisplay.md) <br/> |Gibt den Anzeigenamen eines Formularcontainers zurück.  <br/> |
|[Getlasterror](imapiformcontainer-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formularcontainerobjekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

