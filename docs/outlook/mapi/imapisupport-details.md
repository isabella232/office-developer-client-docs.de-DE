---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d641412a631b60c8f113555b20268cdefb94f2d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630670"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
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
  
> [out] Ein Zeiger auf das Handle zum übergeordneten Fenster des zurückgegebenen Dialogfelds.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das DIALOG_SDI-Kennzeichen angegeben wird. MAPI ruft die **DISMISSMODELESS-Funktion** auf, wenn der Benutzer das Dialogfeld ohne Modusadresse schließt und einen Client, der **IMAPISupport::D etails aufruft,** informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS-Funktion** übergeben werden sollen, auf die der  _Parameter "lpfnDismiss"_ verweist. Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das flag DIALOG_SDI in den  _ulFlags-Parameter_ eingeschlossen wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner, für den Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON-Funktion](lpfnbutton.md) basiert. Eine **LPFNBUTTON-Funktion** fügt dem Detaildialogfeld eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _Parameter lpfButtonCallback_ angegebene Funktion verwendet werden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche benötigt wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Das folgende Kennzeichen kann festgelegt werden: 
    
DIALOG_MODAL
  
> Zeigt die modale Version des allgemeinen Adressdialogfelds an. Dieses Kennzeichen schließen sich mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
>  Zeigt die moduslose Version des allgemeinen Adressdialogfelds an. Dieses Kennzeichen schließen sich mit DIALOG_MODAL gegenseitig aus. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld "Details" wurde für den Adressbucheintrag erfolgreich angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D etails-Methode** wird für Adressbuchanbieter-Supportobjekte implementiert. Adressbuchanbieter rufen **Details** auf, um ein Dialogfeld anzuzeigen, in dem Details zu einem bestimmten Eintrag im Adressbuch angezeigt werden. Die Parameter  _lpfButtonCallback,_  _lpvButtonContext_ und  _lpszButtonText_ können verwendet werden, um dem Dialogfeld eine clientdefinierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die durch  _lpfButtonCallback_ verwiesen wird, wobei sowohl der Eintragsbezeichner der Schaltfläche als auch die Daten in  _lpvButtonContext_ übergeben werden. Wenn keine erweiterbare Schaltfläche erforderlich ist, sollte  _lpszButtonText_ NULL sein. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

