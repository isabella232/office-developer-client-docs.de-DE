---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413059"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Formularanzeigen, Informationen zu Formularservern zu erhalten und zu aktivieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Form-Manager-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Formularbibliotheken  <br/> |
|Aufgerufen von:  <br/> |Formularanzeigen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormMgr  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Startet ein Formular zum Öffnen einer vorhandenen Nachricht.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Löst eine Nachrichtenklasse in ihr Formular in einem Formularcontainer auf und gibt ein Formularinformationsobjekt für dieses Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Löst eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formularcontainer auf und gibt ein Array von Formularinformationsobjekten für diese Formulare zurück.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Gibt ein Array der Eigenschaften zurück, die von einer Gruppe von Formularen verwendet werden.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Startet ein Formular, um eine neue Nachricht basierend auf der Nachrichtenklasse des Formulars zu erstellen.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Zeigt ein Dialogfeld an, in dem der Benutzer ein Formular auswählen kann, und gibt ein Formularinformationsobjekt zurück, das dieses Formular beschreibt.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Stellt ein Dialogfeld vor, in dem der Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formularinformationsobjekten zurück, die diese Formulare beschreiben.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Zeigt ein Dialogfeld an, in dem der Benutzer einen Formularcontainer auswählen kann, und gibt eine Schnittstelle für das vom Benutzer ausgewählte Containerobjekt zurück.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Öffnet eine [IMAPIFormContainer-Schnittstelle](imapiformcontaineriunknown.md) für einen bestimmten Formularcontainer.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Lädt ein Formular zum Öffnen herunter.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Bestimmt, ob ein Formular eigene Nachrichtenkonflikte verarbeiten kann.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der für das Formular-Manager-Objekt aufgetreten ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

