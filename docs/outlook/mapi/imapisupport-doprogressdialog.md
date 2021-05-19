---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432583"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft ein Statusobjekt ab, das eine Statusanzeige anzeigt.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster des Statusindikators.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Progress-Objekt den Fortschritt berechnen soll. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für ein Element auf oberster Ebene berechnet, z. B. für einen übergeordneten Ordner. Das progress-Objekt sollte die Werte in den _UlCount-_ und _ulTotal-Parametern_ der [IMAPIProgress::P rogress-Methode](imapiprogress-progress.md) verwenden, die das aktuelle Element bzw. die Gesamtelemente im Vorgang angeben, um die Statusanzeige für den Vorgang zu erhöhen. 
    
 _lppProgress_
  
> [out] Ein Zeiger auf einen Zeiger auf das Progress-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Statusobjekt wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::D oProgressDialog-Methode** wird für Unterstützungsobjekte des Adressbuch- und Nachrichtenspeicheranbieters implementiert. Diese Anbieter rufen **DoProgressDialog auf,** um auf die MAPI-Implementierung der [IMAPIProgress-Schnittstelle](imapiprogressiunknown.md) zu zugreifen, die die Statusinformationen berechnet und ein Standarddialogfeld anzeigt. 
  
Informationen zur Verwendung eines Statusobjekts und der **IMAPIProgress-Schnittstelle** finden Sie unter [Display a Progress Indicator](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)

