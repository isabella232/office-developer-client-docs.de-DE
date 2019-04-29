---
title: HrOpenABEntryWithProviderUIDSupport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1fafc810-7cf3-4c8c-bf21-055ae34da690
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da40e240b60fa42c48185600b74c6162a966e6f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409545"
---
# <a name="hropenabentrywithprovideruidsupport"></a>HrOpenABEntryWithProviderUIDSupport

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt die gleiche Funktion wie die [HrOpenABEntryWithProviderUID](hropenabentrywithprovideruid.md) -Funktion aus, mit der Ausnahme, dass die **HrOpenABEntryWithProviderUIDSupport** -Funktion den Eintrag mit dem angegebenen Support Objekt öffnet, statt die Sitzung und das Adressbuch zu verwenden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUIDSupport(
  const MAPIUID *pEmsabpUID,
  LPMAPISUP lpSup,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _pEmsabpUID_
  
> in Ein Zeiger auf einen _emsabpUID_ -Parameter, der den Exchange-Adressbuchanbieter identifiziert, der von dieser Funktion verwendet werden soll, um Details zur Eintrags-ID anzuzeigen. Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf wirkt genau wie [IAddrBook::D ails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, wirkt sich diese Funktion auch genau wie [IAddrBook::D ails](iaddrbook-details.md).
    
 _lpSup_
  
> 
    
 _cbEntryID_
  
> in Die Bytezahl der vom _lpEntryID_ -Parameter angegebenen Eintrags-ID. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID, die den zu öffnenden Adressbucheintrag darstellt.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) der Schnittstelle, die für den Zugriff auf den geöffneten Eintrag verwendet werden soll. Beim Übergeben von NULL wird die Standardschnittstelle des Objekts zurückgegeben. Für Messagingbenutzer ist die Standardschnittstelle [IMailUser: IMAPIProp](imailuserimapiprop.md). Für Verteilerlisten ist es [IDistList: IMAPIContainer](idistlistimapicontainer.md), und für Container ist es [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Anrufer können _lpInterface_ auf die entsprechende Standardschnittstelle oder eine Schnittstelle in der Vererbungshierarchie festlegen. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert. Die folgenden Flags können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details TRUE zurückgegeben werden, wenn tatsächlich Änderungen an der Adresse vorgenommen werden. Andernfalls gibt Details FALSE zurück.
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.
    
DIALOG_SDI
  
> Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen.
    
MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Eintrags.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger des geöffneten Eintrags.
    

