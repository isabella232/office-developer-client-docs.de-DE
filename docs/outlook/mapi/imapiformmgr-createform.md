---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419849"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Formular zum Erstellen einer neuen Nachricht auf der Grundlage der Nachrichtenklasse des Formulars.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster für die Statusanzeige, die angezeigt wird, während das Formular geöffnet wird. Der _ulUIParam_ -Parameter wird ignoriert, es sei denn, das MAPI_DIALOG-Flag wird im _ulFlags_ -Parameter festgelegt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Formular geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche an, um den Status anzugeben oder den Benutzer aufzufordern, weitere Informationen zu erhalten. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrminfoToActivate_
  
> in Ein Zeiger auf das Formular Informationsobjekt, das zum Öffnen des Formulars verwendet wird.
    
 _refiidToAsk_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID) für die Schnittstelle für das erstellte Formularobjekt zurückgegeben werden. Der _refiidToAsk_ -Parameter darf nicht NULL sein. 
    
 _ppvObj_
  
> Out Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Die angeforderte Schnittstelle wird vom Form-Objekt nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormMgr:: CreateForm** -Methode auf, um ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars zu öffnen. **CreateForm** öffnet das Formular, indem eine Instanz des Formular Servers für dieses Formular erstellt wird, wie im angegebenen Formular Informationsobjekt beschrieben. Bei Bedarf ruft **CreateForm** die [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) -Methode auf, um den Formularserver Code auf den Datenträger des Benutzers herunterzuladen. 
  
Der Parameter _pfrminfoToActivate_ muss auf ein Formular Informationsobjekt zeigen, das korrekt aufgelöst wurde. 
  
Nachdem das Formular geöffnet wurde, muss der aufrufende Formular Betrachter eine Nachricht mithilfe der [IPersistMessage](ipersistmessageiunknown.md) -Schnittstelle einrichten und optional einen Ansichtskontext für das Formular einrichten. Weitere Informationen finden Sie unter [Starten eines Formular Servers](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI verwendet die **IMAPIFormMgr:: CreateForm** -Methode, um ein Formular zu erstellen, bevor es angezeigt wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Starten eines Formular Servers](launching-a-form-server.md)

