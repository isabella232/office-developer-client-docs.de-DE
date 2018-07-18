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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792375"
---
# <a name="imapisupportdoprogressdialog"></a>IMAPISupport::DoProgressDialog

  
  
**Betrifft**: Outlook 
  
Ruft ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt Fortschritt Fortschritt berechnen soll. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Status für ein Element der obersten Ebene wie beispielsweise einen übergeordneten Ordner berechnet wird. Das Objekt Fortschritt sollte verwenden Sie die Werte in [IMAPIProgress::Progress](imapiprogress-progress.md) _UlCount_ und _UlTotal_ Methodenparameter – die das aktuelle Element und die insgesamt Elemente bei der Konflikte jeweils angeben – um den Fortschritt zu erhöhen Symbol für den Vorgang. 
    
 _lppProgress_
  
> [out] Ein Zeiger auf einen Zeiger auf das Objekt ausgeführt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Fortschritt-Objekt wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::DoProgressDialog** -Methode wird für Adresse Adressbuch und Nachricht Store Anbieter Unterstützungsobjekte implementiert. Diese Anbieter Aufrufen **DoProgressDialog** Zugriff auf die MAPI-Implementierung der [IMAPIProgress](imapiprogressiunknown.md) -Schnittstelle, die berechnet der Fortschrittsinformationen und ein standard-Dialogfeld angezeigt. 
  
Informationen zur Verwendung eines Objekts des Fortschritts und der **IMAPIProgress** -Schnittstelle finden Sie unter [Display eine Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)

