---
title: IAddrBookDetails
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Details
api_type:
- COM
ms.assetid: 4eee4382-98c3-4714-8920-8d72edef00b8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21905af0f4215dc5d25c4d768a5ecff9d0447b60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616859"
---
# <a name="iaddrbookdetails"></a>IAddrBook::Details

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.
  
```cpp
HRESULT Details(
  ULONG_PTR FAR * lpulUIParam,
  LPFNDISMISS lpfnDismiss,
  LPVOID lpvDismissContext,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPFNBUTTON lpfButtonCallback,
  LPVOID lpvButtonContext,
  LPSTR lpszButtonText,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpulUIParam_
  
> [in] Ein Zeiger auf ein Handle des übergeordneten Fensters für das Dialogfeld.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das DIALOG_SDI-Kennzeichen angegeben wird. MAPI ruft die **DISMISSMODELESS-Funktion** auf, wenn der Benutzer das Dialogfeld ohne Modusadresse schließt und einen Client, der **Details** aufruft, darüber informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS-Funktion** übergeben werden sollen, auf die der  _Parameter "lpfnDismiss"_ verweist. Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das flag DIALOG_SDI in den  _ulFlags-Parameter_ eingeschlossen wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner für den Eintrag, für den Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON-Funktion](lpfnbutton.md) basiert. Eine **LPFNBUTTON-Funktion** fügt dem Detaildialogfeld eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _Parameter lpfButtonCallback_ angegebene Funktion verwendet wurden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _parameter lpszButtonText_ sollte NULL sein, wenn Sie keine erweiterbare Schaltfläche benötigen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Die folgenden Flags können festgelegt werden: 
    
AB_TELL_DETAILS_CHANGE
  
> Gibt an, dass **Details** S_OK zurückgibt, ob änderungen an der Adresse tatsächlich vorgenommen werden; andernfalls **gibt Details** S_FALSE zurück. 
    
DIALOG_MODAL
  
> Zeigt die modale Version des allgemeinen Adressdialogfelds an, das immer in Nicht-Outlook-Clients angezeigt wird. Dieses Kennzeichen schließen sich mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
>  Zeigt die moduslose Version des allgemeinen Adressdialogfelds an. Dieses Kennzeichen wird für Nicht-Outlook-Clients ignoriert. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld "Details" wurde für den Adressbucheintrag erfolgreich angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Clientanwendungen rufen die Details-Methode auf, um ein Dialogfeld anzuzeigen, in dem Details zu einem bestimmten Eintrag im Adressbuch angezeigt werden.  Sie können die Parameter  _lpfButtonCallback,_  _lpvButtonContext_ und  _lpszButtonText_ verwenden, um dem Dialogfeld eine clientdefinierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die durch  _lpfButtonCallback_ verwiesen wird, wobei sowohl der Eintragsbezeichner der Schaltfläche als auch die Daten in  _lpvButtonContext_ übergeben werden. Wenn Sie keine erweiterbare Schaltfläche benötigen, sollte  _lpszButtonText_ NULL sein. 
  
 **Details** unterstützen Unicode-Zeichenzeichenfolgen; Unicode-Zeichenfolgen werden in das MBCS-Format (Multibyte Character String) konvertiert, bevor sie im Detaildialogfeld angezeigt werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnOpenEntryID  <br/> |MFCMAPI verwendet die **Detailmethode,** um ein Dialogfeld anzuzeigen, in dem die Details für einen Adressbucheintrag angezeigt werden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

