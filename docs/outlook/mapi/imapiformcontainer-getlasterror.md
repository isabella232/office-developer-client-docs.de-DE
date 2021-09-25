---
title: IMAPIFormContainerGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormContainer.GetLastError
api_type:
- COM
ms.assetid: 04952b51-f005-4933-a1d1-695c6dc736cc
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc7e160f679e3fd3acae35d0f4b8596227a96b75
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630810"
---
# <a name="imapiformcontainergetlasterror"></a>IMAPIFormContainer::GetLastError

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Fehler enthält, der vom Formularcontainerobjekt generiert wurde. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameter

 _Hresult_
  
> [in] Ein HRESULT-Datentyp, der den Fehlerwert enthält, der im vorherigen Methodenaufruf generiert wurde.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen in der [MAPIERROR-Struktur,](mapierror.md) die im  _Parameter lppMAPIError_ zurückgegeben werden, weisen das Unicode-Format auf. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
 _lppMAPIError_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene **MAPIERROR-Struktur,** die Versions-, Komponenten- und Kontextinformationen für den Fehler enthält. Der  _lppMAPIError-Parameter_ kann auf NULL festgelegt werden, wenn keine **MAPIERROR-Struktur** zurückgegeben werden soll. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und **GetLastError** unterstützt unicode nicht, oder MAPI_UNICODE nicht festgelegt wurde und **GetLastError** nur Unicode unterstützt. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFormContainer::GetLastError-Methode** liefert Informationen zu einem vorherigen Fehlgeschlagenen Methodenaufruf. Anrufer können ihren Benutzern detaillierte Informationen zu dem Fehler bereitstellen, indem sie die Daten aus der **MAPIERROR-Struktur** in ein Dialogfeld einschließen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **MAPIERROR-Struktur verwenden,** auf die durch den  _lppMAPIError-Parameter_ verwiesen wird, wenn MAPI nur dann eine bereitstellt, wenn **GetLastError** S_OK zurückgibt. Manchmal kann die MAPI nicht ermitteln, was der letzte Fehler war, oder sie kann nichts mehr über den Fehler berichten. In diesem Fall wird stattdessen ein Zeiger auf NULL in  _lppMAPIError_ zurückgegeben. 
  
Weitere Informationen zur **GetLastError** -Methode finden Sie unter [Verwenden erweiterter Fehler.](mapi-extended-errors.md)
  
## <a name="see-also"></a>Siehe auch



[MAPIERROR](mapierror.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

