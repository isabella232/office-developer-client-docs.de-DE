---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b3803a416f81a47f01532ac865df93135cc6420
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610797"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen XML-Datenstrom (Extensible Markup Language) zurück, der Informationen darstellt, die vom AutoErmittlungsdienst eines Microsoft Exchange 2007-Servers abgerufen wurden.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |olmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Parameter

 _pwzAddress_
  
> [in] Eine MIT NULL beendete SMTP-E-Mail-Adresse (Simple Mail Transfer Protocol) des Kontos, für das Sie die AutoErmittlungsinformationen abrufen möchten.
    
 _pwzPassword_
  
> [in] Ein optionales Kennwort für das von  _pwzAddress_ angegebene Konto. Beachten Sie, dass das Übergeben eines Kennworts keine Auswirkung hat, wenn für das von  _pwzAddress_ angegebene Konto kein Kennwort erforderlich ist. 
    
 _hCancelEvent_
  
> [in] Ein nicht festgelegtes Win32-Ereignishandle, das optional ist und zum Abbrechen des Vorgangs verwendet werden kann. Um den Vorgang abzubrechen, legen Sie das Ereignis fest und übergeben das Ereignishandle als  _hCancelEvent;_ übergeben **Sie NULL,** wenn Sie den Vorgang nicht abbrechen möchten. Beachten Sie, dass das Übergeben eines Werts, der kein Ereignishandle darstellt, keine Auswirkung hat und von der Funktion ignoriert wird. 
    
 _ulFlags_
  
> [in] Dieser Parameter wird nicht verwendet. Es muss 0 sein.
    
 _ppXmlStream_
  
> [out] Ein Zeiger auf ein [IStream-Objekt,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) das die AutoDiscovery-XML enthält. Gibt **NULL zurück,** wenn der AutoDiscovery-Vorgang fehlschlägt. Sie müssen das [IStream-Objekt](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) freigeben, wenn Sie damit fertig sind. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK 
  
- Der Funktionsaufruf ist erfolgreich.
    
E_INVALIDARG 
  
-  _pwzAddress_ ist **NULL** oder ist keine gültige SMTP-Adresse, oder _ppXmlStream_ ist ein **NULL-Zeiger** auf ein [IStream-Objekt.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- Clientcomputer ist nicht mit dem Netzwerk verbunden, Clientcomputer ist nicht mit einem Microsoft Exchange 2007-Server verbunden, _pwzAddress_ ist kein Konto auf einem Exchange 2007-Server oder _pwzAddress_ ist ein Konto, das Exchange AutoErmittlungsdienst nicht unterstützt. 
    
MAPI_E_USER_CANCEL 
  
- Ein Ereignishandle wurde an  _hCancelEvent_ übergeben, um den Vorgang abzubrechen. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Der an  _pwzAddress_ oder  _pwzPassword_ übergebene Wert ist zu lang, sodass er den internen Puffer von 256 Byte überläuft. 
    

