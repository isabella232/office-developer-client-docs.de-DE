---
title: HrDoABDetailsWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 27741887-8405-49ed-b080-613613faf91b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7d46d400263cc3ab0ef6cf19689abbdfc4fcae66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584514"
---
# <a name="hrdoabdetailswithprovideruid"></a>HrDoABDetailsWithProviderUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, dass die **OpenEntry-Methode** vom erwarteten Exchange Adressbuchanbieter geöffnet wird. Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails,](iaddrbook-details.md) öffnet aber **entryID** mithilfe des von _pEmsabpUID identifizierten_ Exchange Adressbuchs.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrDoABDetailsWithProviderUID(
  const MAPIUID   *pEmsabpUID,
  LPADRBOOK        pAddrBook,
  ULONG_PTR FAR *  lpulUIParam,
  LPFNDISMISS      lpfnDismiss,
  LPVOID           lpvDismissContext,
  ULONG            cbEntryID,
  LPENTRYID        lpEntryID,
  LPFNBUTTON       lpfButtonCallback,
  LPVOID           lpvButtonContext,
  LPSTR           lpszButtonText,
  ULONG            ulFlags
);
```

## <a name="parameters"></a>Parameter

 _pEmsabpUID_
  
> [in] Ein Zeiger auf eine _emsabpUID,_ die den Exchange Adressbuchanbieter identifiziert, den diese Funktion verwenden sollte, um Details zum Eintragsbezeichner anzuzeigen. Wenn der Bezeichner für den eingehenden Eintrag kein Exchange Adressbuchanbieter-Eintragsbezeichner ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich genau wie [IAddrBook::D etails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine Null MAPIUID ist, verhält sich diese Funktion auch genau wie [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _lpulUIParam_
  
> [out] Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem **DISMISSMODELESS-Prototyp** oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das DIALOG_SDI-Kennzeichen angegeben wird. MAPI ruft die **DISMISSMODELESS-Funktion** auf, wenn der Benutzer das Dialogfeld ohne Modusadresse schließt und einen Client, der Details aufruft, darüber informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS-Funktion** übergeben werden sollen, auf die der  _Parameter "lpfnDismiss"_ verweist. Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das **flag DIALOG_SDI** in den  _ulFlags-Parameter_ eingeschlossen wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl des Eintragsbezeichners, der durch den  _lpEntryID-Parameter_ angegeben wird. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner, der den zu öffnenden Adressbucheintrag darstellt.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem Prototyp der **LPFNBUTTON-Funktion** basiert. Eine **LPFNBUTTON-Funktion** fügt dem Detaildialogfeld eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _Parameter lpfButtonCallback_ angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche benötigt wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Die folgenden Flags können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass Details TRUE zurückgibt, wenn Änderungen an der Adresse tatsächlich vorgenommen werden; andernfalls gibt Details FALSE zurück.
    
DIALOG_MODAL
  
> Zeigt die modale Version des allgemeinen Adressdialogfelds an. Dieses Kennzeichen schließen sich mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
> Zeigt die moduslose Version des allgemeinen Adressdialogfelds an. Dieses Kennzeichen schließen sich mit DIALOG_MODAL gegenseitig aus.
    
MAPI_UNICODE
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    

