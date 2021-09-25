---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de99531801c72397f37d3de9e9bf9d61b9a7f74b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556630"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Lädt ein Formular zum Öffnen herunter.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die angezeigt wird, während das Formular heruntergeladen wird. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das flag MAPI_DIALOG im  _UlFlags-Parameter_ festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Formular heruntergeladen wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status bereitzustellen oder den Benutzer zur Eingabe weiterer Informationen aufzufordern. Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrmiInfo_
  
> [in] Ein Zeiger auf ein Formularinformationsobjekt für das herunterzuladende Formular.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormMgr::P repareForm-Methode** auf, um ein Formular aus einem Formularcontainer zum Öffnen herunterzuladen. Die meisten Formularviewer müssen **PrepareForm** nicht aufrufen, da die Methoden [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) und [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) bei Bedarf **PrepareForm** aufrufen. 
  
Sie können **PrepareForm** verwenden, um die Dynamic Link Libraries (DLLs) und andere Dateien, die einem Formular zugeordnet sind, abzurufen, um sie zu ändern. Wenn das geänderte Formular wieder in den Formularcontainer geladen wird, muss es neu installiert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

