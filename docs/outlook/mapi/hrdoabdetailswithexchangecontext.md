---
title: HrDoABDetailsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b4e7fed2-88e4-4e14-90b6-913a1b7e338a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e041597a01774fcdda3d99532bf5b062acdd46ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584535"
---
# <a name="hrdoabdetailswithexchangecontext"></a>HrDoABDetailsWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt sicher, dass die **OpenEntry-Methode** vom erwarteten Exchange Adressbuchanbieter geöffnet wird. Diese Funktion funktioniert ähnlich wie [IAddrBook::D etails,](iaddrbook-details.md)öffnet jedoch die **entryID** mithilfe des Exchange Adressbuchs, das durch den _Parameter "pEmsmdbUID"_ identifiziert wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithExchangeContext(
  LPMAPISESSION   pmsess,
  const MAPIUID  *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags,
);
```

## <a name="parameters"></a>Parameter

 _pmsess_
  
> Die angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> Ein Zeiger auf eine **emsmdbUID,** die den Exchange Dienst identifiziert, der den Exchange Adressbuchanbieter enthält, der von der Funktion zum Öffnen des Eintragsbezeichners verwendet wird. Wenn der Bezeichner für den eingehenden Eintrag kein Exchange Adressbuchanbieter-Eintragsbezeichner ist, wird dieser Parameter ignoriert, und die Funktion verhält sich wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). Wenn dieser Parameter NULL oder eine Null **MAPIUID** ist, verhält sich diese Funktion auch genau wie [IAddrBook::OpenEntry](iaddrbook-openentry.md). 
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _lpulUIParam_
  
> [out] Ein Handle für das übergeordnete Fenster für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem **DISMISSMODELESS-Prototyp** oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festzulegende DIALOG_SDI-Kennzeichen angegeben. MAPI ruft die **DISMISSMODELESS-Funktion** auf, wenn der Benutzer das Dialogfeld ohne Modusadresse schließt und einen Client, der Details aufruft, darüber informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
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
    

