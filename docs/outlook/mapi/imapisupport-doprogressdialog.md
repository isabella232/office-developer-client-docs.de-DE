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
  
Ruft ein Progress-Objekt ab, das eine Statusanzeige anzeigt.
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Berechnung des Fortschritts durch das Progress-Objekt steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für ein Element auf oberster Ebene, wie beispielsweise einen übergeordneten Ordner, berechnet. Das Progress-Objekt sollte die Werte in den Parametern _ulCount_ und _ulTotal_ der [IMAPIProgress::P rogress](imapiprogress-progress.md) -Methode verwenden, die das aktuelle Element und die gesamten Elemente in der Operation angeben, um den Fortschritt zu erhöhen. Indikator für den Vorgang. 
    
 _lppProgress_
  
> Out Ein Zeiger auf einen Zeiger auf das Progress-Objekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Progress-Objekt wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D oprogressdialog** -Methode wird für Support Objekte des Adressbuchs und des Nachrichtenspeichers implementiert. Diese Anbieter rufen **DoProgressDialog** auf, um auf die MAPI-Implementierung der [IMAPIProgress](imapiprogressiunknown.md) -Schnittstelle zuzugreifen, die die Fortschrittsinformationen berechnet und ein Standarddialogfeld anzeigt. 
  
Informationen zur Verwendung eines Progress-Objekts und der **IMAPIProgress** -Schnittstelle finden Sie unter [Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md).
  
## <a name="see-also"></a>Siehe auch



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)

