---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417364"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht Clientanwendungen Zugriff auf Eigenschaften, die für die Formulardefinition besonders sind. Wenn Formularinformationen in einem separaten Objekt gespeichert werden, kann der Formularbibliotheksanbieter ein Formular für einen Client beschreiben, ohne das Formular zu aktivieren.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularinformationsobjekte  <br/> |
|Implementiert von:  <br/> |Anbieter von Formularbibliotheken  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormInfo  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMINFO  <br/> |
|Transaktionsmodell:  <br/> |Nichttransaktioniert  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften zurück, den ein Formular verwendet.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, den ein Formular verwendet.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Gibt einen Zeiger auf den Formularcontainer zurück, in dem ein bestimmtes Formular installiert ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Im Gegensatz zu den meisten in der MapiForm.h-Headerdatei definierten Schnittstellen erbt **IMAPIFormInfo** von der [IMAPIProp-Schnittstelle,](imapipropiunknown.md) da die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) exportiert werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

