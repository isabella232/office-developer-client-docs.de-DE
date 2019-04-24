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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322358"
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
  
> Out Ein Zeiger auf das Handle des übergeordneten Fensters des zurückgegebenen Dialogfelds.
    
 _lpfnDismiss_
  
> in Ein Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS](dismissmodeless.md) -Prototyp basiert, oder NULL. Dieses Element gilt nur für die nicht modale Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI-Flag angegeben. MAPI Ruft die **DISMISSMODELESS** -Funktion auf, wenn der Benutzer das Dialogfeld nicht modale Adresse abschließt und einen Client informiert, der **IMAPISupport::D ails** , dass das Dialogfeld nicht mehr aktiv ist. 
    
 _lpvDismissContext_
  
> in Ein Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS** -Funktion übergeben werden, auf die durch den _lpfnDismiss_ -Parameter verwiesen wird. Dieser Parameter gilt nur für die nicht modale Version des Dialogfelds, indem das DIALOG_SDI-Flag im _ulFlags_ -Parameter eingeschlossen wird. 
    
 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID, für die Details angezeigt werden.
    
 _lpfButtonCallback_
  
> in Ein Zeiger auf eine Funktion, die auf dem Prototyp der [LPFNBUTTON](lpfnbutton.md) -Funktion basiert. Mit einer **LPFNBUTTON** -Funktion wird dem Dialogfeld Details eine Schaltfläche hinzugefügt. 
    
 _lpvButtonContext_
  
> in Ein Zeiger auf Daten, die als Parameter für die durch den _lpfButtonCallback_ -Parameter angegebene Funktion verwendet werden. 
    
 _lpszButtonText_
  
> in Ein Zeiger auf eine Zeichenfolge, die den Text enthält, der auf die hinzugefügte Schaltfläche angewendet werden soll, wenn diese Schaltfläche erweiterbar ist. Der Parameter _lpszButtonText_ sollte NULL sein, wenn eine erweiterbare Schaltfläche nicht erforderlich ist. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp für den _lpszButtonText_ -Parameter steuert. Das folgende Flag kann festgelegt werden: 
    
DIALOG_MODAL
  
> Zeigt die modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_SDI gegenseitig ausschließen.
    
DIALOG_SDI
  
>  Zeigt die nicht modale Version des Dialogfelds allgemeine Adresse an. Dieses Flag ist mit DIALOG_MODAL gegenseitig ausschließen. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Dialogfeld Details wurde erfolgreich für den Adressbucheintrag angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D ails** -Methode wird für Support Objekte des Adressbuch Anbieters implementiert. Adressbuchanbieter rufen **Details** auf, um ein Dialogfeld anzuzeigen, in dem Details zu einem bestimmten Eintrag im Adressbuch angezeigt werden. Der Parameter _lpfButtonCallback_, _lpvButtonContext_und _lpszButtonText_ kann verwendet werden, um dem Dialogfeld eine Client definierte Schaltfläche hinzuzufügen. Wenn auf die Schaltfläche geklickt wird, ruft MAPI die Rückruffunktion auf, auf die von _lpfButtonCallback_verwiesen wird, wobei sowohl die Eintrags-ID der Schaltfläche als auch die Daten in _lpvButtonContext_übergeben werden. Wenn keine erweiterbare Schaltfläche erforderlich ist, sollte _LPSZBUTTONTEXT_ NULL sein. 
  
## <a name="see-also"></a>Siehe auch



[ADRPARM](adrparm.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[LPFNBUTTON](lpfnbutton.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

