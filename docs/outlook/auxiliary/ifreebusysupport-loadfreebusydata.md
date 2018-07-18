---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer, eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen innerhalb eines Zeitraums.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790963"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Gibt für jeden angegebenen Benutzer, eine Schnittstelle zum Aufzählen Datenblöcke Frei/Gebucht-Informationen innerhalb eines Zeitraums. 
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parameter

_cMax_
  
> [in] Die Anzahl der zurückzugebenden [IFreeBusyData](ifreebusydata.md) -Schnittstellen. 
    
_rgfbuser_
  
> [in] Das Array von Frei/Gebucht-Informationen abrufen von Daten für Benutzer.
    
_prgfbdata_
  
> [in] [out] Das Array von **IFreeBusyData** -Schnittstellen, die das _Rgfbuser_ Array von [FBUser](fbuser.md) Strukturen entsprechen. 
    
   > [!NOTE]
   > Dieses Array von Zeigern wird vom Anrufer belegt und vom Anrufer freigegeben. Die tatsächlichen Schnittstellen auf den verwiesen werden freigegeben, wenn der Aufrufer diese nicht mehr benötigt wird. 
  
_phrStatus_
  
> [out] Das Array von **HRESULT** -Ergebnisse für jede entsprechende **IFreeBusyData** -Schnittstelle abrufen. Der Wert kann NULL sein. Ein Ergebnis wird auf S_OK festgelegt, wenn die entsprechenden _Prgfbdata_ gültig ist. 
    
_pcRead_
  
>  [out] Die tatsächliche Anzahl von Benutzern für die eine **IFreeBusyData** Schnittstelle gefunden wurde. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)

