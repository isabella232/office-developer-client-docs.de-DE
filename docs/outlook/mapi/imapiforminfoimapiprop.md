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
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575910"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Client Applications Zugriff auf Eigenschaften, die speziell für Formulardefinition gelten. Hält Formularinformationen in einem separaten Objekt, kann der Formular Bibliotheksanbieter ein Formulars an einen Client beschreiben, ohne das Formular aktivieren.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verfügbar gemacht von:  <br/> |Formular Informationen-Objekte  <br/> |
|Implementiert von:  <br/> |Anbieter für Formular-Bibliothek  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormInfo  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMINFO  <br/> |
|Transaktionsmodell:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften, die einem Formular verwendet wird.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Verben, die ein Formular verwendet wird.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Erstellt ein Symbol aus einer Icon-Eigenschaft eines Formulars an.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Gibt einen Zeiger auf den Formular-Container, in dem ein bestimmtes Formular installiert ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zu den meisten Schnittstellen in der Headerdatei MapiForm.h definiert erbt **IMAPIFormInfo** über die Benutzeroberfläche [IMAPIProp](imapipropiunknown.md) , da es die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode exportiert. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

