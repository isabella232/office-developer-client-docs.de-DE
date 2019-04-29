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
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige, das angezeigt wird, während das Formular heruntergeladen wird. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Herunterladen des Formulars steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status anzugeben oder den Benutzer aufzufordern, weitere Informationen zu erhalten. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrmiInfo_
  
> in Ein Zeiger auf ein Formular Informationsobjekt für das Formular heruntergeladen werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr::P repareform** -Methode auf, um ein Formular aus einem Formular Container zum Öffnen herunterzuladen. Die meisten Formular Betrachter müssen **PrepareForm**nicht aufrufen, da die Methoden [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) und [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) **PrepareForm**bei Bedarf aufrufen. 
  
Sie können **PrepareForm** verwenden, um die DLLs (Dynamic Link Libraries) und andere Dateien abzurufen, die einem Formular zugeordnet sind, um Sie zu ändern. Wenn das geänderte Formular wieder in seinen Formular Container geladen wird, muss es erneut installiert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

