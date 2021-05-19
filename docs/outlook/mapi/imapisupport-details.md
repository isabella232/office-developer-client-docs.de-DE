---
title: IMAPISupportDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Details
api_type:
- COM
ms.assetid: 1a62efa2-dd6b-4acb-a760-defa601c20c9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bdc57a6e951e54640fe3c638977c6a5f16986e68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426779"
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
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt, und informiert einen Client, der **IMAPISupport::D etails aufruft,** dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen, der an die **DISMISSMODELESS-Funktion übergeben** wird, auf die der  _lpfnDismiss-Parameter_ verweist. Dieser Parameter gilt nur für die moduslose Version des Dialogfelds, indem das DIALOG_SDI im  _ulFlags-Parameter verwendet_ wird. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID, für die Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion basierend auf dem [LPFNBUTTON-Funktionsprototyp.](lpfnbutton.md) Eine **LPFNBUTTON-Funktion** fügt dem Dialogfeld Details eine Schaltfläche hinzu. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die durch den  _lpfButtonCallback-Parameter_ angegebene Funktion verwendet werden. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der  _lpszButtonText-Parameter_ sollte NULL sein, wenn keine erweiterbare Schaltfläche erforderlich ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp für den  _lpszButtonText-Parameter_ steuert. Das folgende Flag kann festgelegt werden: 
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_SDI.
    
DIALOG_SDI
  
>  Zeigt die moduslose Version des Dialogfelds allgemeine Adresse an. Dieses Flag schließen sich gegenseitig mit DIALOG_MODAL. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::D etails-Methode** wird für Unterstützungsobjekte des Adressbuchanbieters implementiert. Adressbuchanbieter rufen **Details auf,** um ein Dialogfeld anzuzeigen, das Details zu einem bestimmten Eintrag im Adressbuch enthält. Die  _Parameter lpfButtonCallback,_  _lpvButtonContext_ und  _lpszButtonText_ können verwendet werden, um dem Dialogfeld eine clientdefinierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_ verwiesen wird. Dabei wird sowohl der Eintragsbezeichner der Schaltfläche als auch die Daten in _lpvButtonContext übergeben._ Wenn keine erweiterbare Schaltfläche erforderlich ist,  _sollte lpszButtonText_ NULL sein. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

