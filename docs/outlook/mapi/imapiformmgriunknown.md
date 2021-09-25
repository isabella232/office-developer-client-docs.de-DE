---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e2d493dd4a0a244363a5405701498c5a96c76870
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571773"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Es Formularviewern, Informationen zu Formularservern abzurufen und diese zu aktivieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formular-Manager-Objekte  <br/> |
|Implementiert von:  <br/> |Formularbibliotheksanbieter  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormMgr  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Startet ein Formular, um eine vorhandene Nachricht zu öffnen.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in ihrem Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften zurück, die eine Gruppe von Formularen verwendet.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Startet ein Formular, um eine neue Nachricht basierend auf der Nachrichtenklasse des Formulars zu erstellen.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Stellt ein Dialogfeld dar, in dem der Benutzer ein Formular auswählen kann, und gibt ein Formularinformationsobjekt zurück, das dieses Formular beschreibt.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Stellt ein Dialogfeld dar, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Stellt ein Dialogfeld dar, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Öffnet eine [IMAPIFormContainer-Schnittstelle](imapiformcontaineriunknown.md) für einen bestimmten Formularcontainer.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Lädt ein Formular zum Öffnen herunter.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Bestimmt, ob ein Formular eigene Nachrichtenkonflikte behandeln kann.  <br/> |
|[Getlasterror](imapiformmgr-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formular-Manager-Objekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

