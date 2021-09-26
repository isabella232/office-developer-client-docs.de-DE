---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 65c00ba95a38005b953e704eafa76cf5e2df4e77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610587"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Clientanwendungen Zugriff auf Eigenschaften, die für die Formulardefinition eignen. Durch das Aufbewahren von Formularinformationen in einem separaten Objekt kann der Formularbibliotheksanbieter ein Formular einem Client beschreiben, ohne das Formular zu aktivieren.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Formularinformationsobjekte  <br/> |
|Implementiert von:  <br/> |Formularbibliotheksanbieter  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPIFormInfo  <br/> |
|Zeigertyp:  <br/> |LPMAPIFORMINFO  <br/> |
|Transaktionsmodell:  <br/> |Nicht übersetzt  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Eigenschaften zurück, die ein Formular verwendet.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Gibt einen Zeiger auf den vollständigen Satz von Verben zurück, die ein Formular verwendet.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Erstellt ein Symbol aus einer Symboleigenschaft eines Formulars.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Speichert eine Beschreibung eines bestimmten Formulars in einer Konfigurationsdatei.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Gibt einen Zeiger auf den Formularcontainer zurück, in dem ein bestimmtes Formular installiert ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zu den meisten Schnittstellen, die in der Headerdatei MapiForm.h definiert sind, erbt **IMAPIFormInfo** von der [IMAPIProp-Schnittstelle,](imapipropiunknown.md) da die meisten Formularinformationen über Aufrufe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) exportiert werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

