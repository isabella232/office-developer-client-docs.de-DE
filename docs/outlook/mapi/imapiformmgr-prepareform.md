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
ms.openlocfilehash: 6e8ea7230ae86dee99cc4413715055fc53afa900
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579725"
---
# <a name="imapiformmgrprepareform"></a>IMAPIFormMgr::PrepareForm

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Downloads für ein Formular zu öffnen.
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige, die angezeigt wird, während das Formular heruntergeladen wird. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Formular heruntergeladen wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrmiInfo_
  
> [in] Ein Zeiger auf ein Formular Informationen-Objekt für das Formular heruntergeladen werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formular Viewer rufen Sie die **IMAPIFormMgr::PrepareForm** -Methode, um ein Formular Container für das Öffnen ein Formulars heruntergeladen werden. Die meisten Formular Viewer müssen nicht **PrepareForm**, aufrufen, da die [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) und die [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) Methoden **PrepareForm**, rufen Sie bei Bedarf. 
  
Sie können **PrepareForm** verwenden, um die Dynamic Link Libraries (DLLs) und andere Dateien, die sie zum Ändern eines Formulars zugeordnet abzurufen. Wenn das geänderte Formular wieder in dessen Container Formular geladen wird, muss es neu installiert werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)
  
[IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

