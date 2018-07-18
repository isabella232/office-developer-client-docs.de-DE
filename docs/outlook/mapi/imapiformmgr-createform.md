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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ed3f793e4353cf78949a9df3a17dd3997a573f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792175"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Betrifft**: Outlook 
  
Öffnet ein Formular zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster für die Statusanzeige, die angezeigt wird, während das Formular geöffnet wird. Der Parameter _UlUIParam_ wird ignoriert, es sei denn, das Flag MAPI_DIALOG im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Formular geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_DIALOG 
  
> Zeigt eine Benutzeroberfläche zum Bereitstellen von Status oder auffordern, Weitere Informationen. Wenn dieses Flag nicht festgelegt ist, wird keine Benutzeroberfläche angezeigt.
    
 _pfrminfoToActivate_
  
> [in] Ein Zeiger auf das Formular Informationen-Objekt, das zum Öffnen des Formulars verwendet wird.
    
 _refiidToAsk_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID) für die Schnittstelle für das Form-Objekt zurückgegeben werden soll, die erstellt wurde. Der Parameter _RefiidToAsk_ darf nicht NULL sein. 
    
 _ppvObj_
  
> [out] Ein Zeiger auf einen Zeiger auf die zurückgegebene Schnittstelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_INTERFACE 
  
> Die angeforderte Schnittstelle wird von der Form-Objekt nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IMAPIFormMgr::CreateForm** -Methode zum Öffnen eines Formulars zum Erstellen einer neuen Nachricht basierend auf der Nachrichtenklasse des Formulars. **CreateForm** Öffnet das Formular durch das Erstellen einer Instanz des Formular-Servers für das Formular in der angegebenen Form Informationen-Objekt beschrieben. Falls erforderlich, ruft **CreateForm** die [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) -Methode, um die Formularcode Server auf der Festplatte des Benutzers herunterladen. 
  
Der Parameter _PfrminfoToActivate_ muss auf ein Form-Informationsobjekt zeigen, der ordnungsgemäß aufgelöst wurde. 
  
Nach dem das Formular geöffnet wurde, der aufrufende Formular-Viewer muss eingerichtet, eine Meldung über die Benutzeroberfläche [IPersistMessage](ipersistmessageiunknown.md) und optional ein Ansichtskontext für das Formular einrichten kann. Weitere Informationen finden Sie unter [Starten einer Form Server](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormMgr::CreateForm** -Methode zum Erstellen eines Formulars vor dem anzeigen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Starten eines Formularservers](launching-a-form-server.md)

