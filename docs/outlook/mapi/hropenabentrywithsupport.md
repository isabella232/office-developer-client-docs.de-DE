---
title: HrOpenABEntryWithSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eaa988ea-aee1-4066-8c78-2b6c28def5e0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8574264bdb470906cc097cec56b39a943937d11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417644"
---
# <a name="hropenabentrywithsupport"></a>HrOpenABEntryWithSupport

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verwenden Sie diese Funktion nicht.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnende Adressbucheintrag darstellt.
    
 _lpInterface_
  
>  [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Durch Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser : IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist [IDistList : IMAPIContainer](idistlistimapicontainer.md)und für Container [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können  _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Die folgenden Kennzeichen können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details TRUE zurückgibt, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.
    
DIALOG_SDI
  
> Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL.
    
MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

