---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416650"
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
  
> [in] Ein Handle zum übergeordneten Fenster der Statusanzeige, das beim Herunterladen des Formulars angezeigt wird. Der  _ulUIParam-Parameter_ wird ignoriert, es sei denn, das MAPI_DIALOG wird im  _ulFlags-Parameter_ festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Formular heruntergeladen wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status zur Verfügung zu stellen, oder fordert den Benutzer auf, weitere Informationen zu erhalten. Wenn dieses Kennzeichen nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrmiInfo_
  
> [in] Ein Zeiger auf ein Formularinformationsobjekt für das zu herunterladende Formular.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormMgr::P repareForm-Methode** auf, um ein Formular aus einem Formularcontainer zum Öffnen herunterzuladen. Die meisten Formularbetrachter müssen **PrepareForm** nicht aufrufen, da die [Methoden IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) und [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) bei Bedarf **PrepareForm** aufrufen. 
  
Sie können **PrepareForm verwenden,** um die Dynamic Link Libraries (DLLs) und andere Dateien zu erhalten, die einem Formular zugeordnet sind, um sie zu ändern. Wenn das geänderte Formular wieder in den Formularcontainer geladen wird, muss es erneut installiert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

