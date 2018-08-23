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
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581517"
---
# <a name="imapiformmgr--iunknown"></a>IMAPIFormMgr : IUnknown

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ermöglicht das Formular Zuschauer zu Informationen zum Beziehen und Aktivieren von Formular Servern. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Formular-Manager-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter für Formular-Bibliothek  <br/> |
|Aufgerufen von:  <br/> |Formular-Viewer  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormMgr  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMMGR  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[LoadForm](imapiformmgr-loadform.md) <br/> |Startet ein Formular, um eine vorhandene Nachricht zu öffnen.  <br/> |
|[ResolveMessageClass](imapiformmgr-resolvemessageclass.md) <br/> |Eine Nachrichtenklasse in seiner Form innerhalb eines Containers Formular aufgelöst wird, und gibt ein Formular Informationen-Objekt für das Formular zurück.  <br/> |
|[ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |Eine Gruppe von Nachrichtenklassen in ihre Formulare in einem Formular Container aufgelöst wird, und gibt ein Array von Formular Informationen Objekte für diese Formulare.  <br/> |
|[CalcFormPropSet](imapiformmgr-calcformpropset.md) <br/> |Gibt ein Array von Eigenschaften, die eine Gruppe von Formularen verwendet.  <br/> |
|[CreateForm](imapiformmgr-createform.md) <br/> |Öffnet ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars.  <br/> |
|[SelectForm](imapiformmgr-selectform.md) <br/> |Zeigt ein Dialogfeld, mit dem den Benutzer ein Formular auswählen an und gibt ein Form-Informationen-Objekt, das dieses Formular beschreibt.  <br/> |
|[SelectMultipleForms](imapiformmgr-selectmultipleforms.md) <br/> |Zeigt ein Dialogfeld, mit dem den Benutzer mehrere Formulare auswählen kann, und gibt ein Array von Formular Informationsobjekten, die diesen Formularen zu beschreiben.  <br/> |
|[SelectFormContainer](imapiformmgr-selectformcontainer.md) <br/> |Zeigt ein Dialogfeld an, die ermöglicht dem Benutzer das Formular Container auswählen, und gibt eine Schnittstelle für das Containerobjekt der ausgewählten Benutzer an.  <br/> |
|[OpenFormContainer](imapiformmgr-openformcontainer.md) <br/> |Öffnet eine [IMAPIFormContainer](imapiformcontaineriunknown.md) -Schnittstelle für ein bestimmtes Formular Container.  <br/> |
|[PrepareForm](imapiformmgr-prepareform.md) <br/> |Downloads für ein Formular zu öffnen.  <br/> |
|[IsInConflict](imapiformmgr-isinconflict.md) <br/> |Bestimmt, ob ein Formular eine eigene Nachricht Konflikte verarbeitet werden kann.  <br/> |
|[GetLastError](imapiformmgr-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen über den vorherigen Fehler auftritt, auf das Formular-Manager-Objekt enthält.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

