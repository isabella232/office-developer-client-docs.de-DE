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
ms.openlocfilehash: 3c1bfccf635b96dd0744d888e69b4af5b8df0fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587873"
---
# <a name="imapisupportdetails"></a>IMAPISupport::Details

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.
  
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
  
> [out] Ein Zeiger auf das Handle für das übergeordnete Fenster des Dialogfelds zurückgegebene.
    
 _lpfnDismiss_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf dem [DISMISSMODELESS](dismissmodeless.md) Prototyp oder NULL. Dieser Member gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag festgelegt wird. MAPI-Aufrufen die **DISMISSMODELESS** -Funktion, wenn der Benutzer schließt das Dialogfeld ohne Modus Adresse informiert einen Client, der **IMAPISupport::Details** anruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> [in] Ein Zeiger auf Kontextinformationen zum Übergeben an die Funktion **DISMISSMODELESS** an, durch den Parameter _LpfnDismiss_ auf. Dieser Parameter gilt nur für die im Dialogfeld ohne Modus Version durch das DIALOG_SDI-Flag in den Parameter _UlFlags_ einschließen. 
    
 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für die Details angezeigt werden.
    
 _lpfButtonCallback_
  
> [in] Ein Zeiger auf eine Funktion, die basierend auf den [LPFNBUTTON](lpfnbutton.md) Funktionsprototyp. Eine **LPFNBUTTON** -Funktion hinzugefügt im Dialogfeld Details der eine Schaltfläche. 
    
 _lpvButtonContext_
  
> [in] Ein Zeiger auf Daten, die als Parameter für die Funktion, die durch den _LpfButtonCallback_ -Parameter angegebene verwendet. 
    
 _lpszButtonText_
  
> [in] Ein Zeiger auf eine Zeichenfolge, die auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist Text enthält. Der Parameter _LpszButtonText_ sollte NULL sein, wenn eine nicht mehr benötigt wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts für den Parameter _LpszButtonText_ steuert. Das folgende Flag kann festgelegt werden: 
    
DIALOG_MODAL
  
> Die modale Version von der Adresse Standarddialogfeld angezeigt. Dieses Kennzeichen ist mit DIALOG_SDI gegenseitig aus.
    
DIALOG_SDI
  
>  Die ohne Modus Version von der Adresse Standarddialogfeld angezeigt. Dieses Kennzeichen ist mit DIALOG_MODAL gegenseitig aus. 
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Im Dialogfeld Details der wurde erfolgreich für den Adresseintrag Adressbuch angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::Details** -Methode wird für Address Book Anbieter Unterstützungsobjekte implementiert. Von adressbuchanbietern implementierte rufen Sie **Details** , um ein Dialogfeld angezeigt, das Details zu einem bestimmten Eintrag im Adressbuch bietet. Der Parameter _LpfButtonCallback_, _LpvButtonContext_und _LpszButtonText_ können verwendet werden, um das Dialogfeld eine Schaltfläche Client definiert hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Callback-Funktion, die auf den _LpfButtonCallback_, sowohl die Eintrags-ID für die Schaltfläche und die Daten in _LpvButtonContext_übergeben. Falls eine erweiterbare Schaltfläche nicht erforderlich ist, sollte _LpszButtonText_ NULL sein. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

