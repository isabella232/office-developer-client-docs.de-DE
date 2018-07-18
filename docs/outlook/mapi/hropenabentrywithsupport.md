---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 262b1aa2cd4a785b612ac0917b4b24358742ea6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791952"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Betrifft**: Outlook 
  
Verwenden Sie diese Funktion nicht.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithSupport(
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID  lpInterface,
  ULONG  ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _lpSup_
  
> 
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID, die den Adresseintrag Adressbuch öffnen darstellt.
    
 _lpInterface_
  
>  [in] Ein Zeiger auf die Schnittstelle-ID (IID) der Schnittstelle, greifen Sie auf den Eintrag open verwendet werden soll. Übergeben von NULL gibt die standard-Schnittstelle des Objekts zurück. Für die messaging-Benutzer ist der standard-Benutzeroberfläche [IMailUser: IMAPIProp](imailuserimapiprop.md). Verteilerlisten, ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container, es ist [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können auf die entsprechende standard-Schnittstelle oder eine Schnittstelle in der Vererbungshierarchie _LpInterface_ festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details gibt TRUE zurück, wenn die Adresse tatsächlich geändert werden. Details andernfalls FALSE.
    
DIALOG_MODAL
  
> Zeigt die modale Version im Dialogfeld allgemeine Adresse. Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
> Zeigt die allgemeine Adresse im Dialogfeld ohne Modus Version. Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus.
    
PARAMETER MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des Eintrags geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des Eintrags geöffnet.
    

