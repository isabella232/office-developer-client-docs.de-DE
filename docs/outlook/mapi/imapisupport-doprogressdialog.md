---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2941178a46b6cd1323d3ccb8ffe3acd97f631155
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620891"
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
  
> [in] Ein Handle für das übergeordnete Fenster der Statusanzeige.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Statusobjekt den Fortschritt berechnen soll. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_TOP_LEVEL 
  
> Der Fortschritt wird für ein Element der obersten Ebene, z. B. einen übergeordneten Ordner, berechnet. Das Statusobjekt sollte die Werte in den _UlCount-_ und _ulTotal-Parametern_ der [IMAPIProgress::P rogress-Methode](imapiprogress-progress.md) verwenden, die das aktuelle Element bzw. die Gesamtelemente des Vorgangs angeben, um die Statusanzeige für den Vorgang zu erhöhen. 
    
 _lppProgress_
  
> [out] Ein Zeiger auf einen Zeiger auf das Statusobjekt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Statusobjekt wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D oProgressDialog-Methode** ist für Adressbuch- und Nachrichtenspeicheranbieter-Supportobjekte implementiert. Diese Anbieter rufen **DoProgressDialog** auf, um auf die MAPI-Implementierung der [IMAPIProgress-Schnittstelle](imapiprogressiunknown.md) zuzugreifen, die die Statusinformationen berechnet und ein Standarddialogfeld anzeigt. 
  
Informationen zur Verwendung eines Statusobjekts und der **IMAPIProgress-Schnittstelle** finden Sie unter [Anzeigen einer Statusanzeige.](how-to-display-a-progress-indicator.md)
  
## <a name="see-also"></a>Siehe auch



[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Anzeigen einer Statusanzeige](how-to-display-a-progress-indicator.md)

