---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitraums zurück.
ms.openlocfilehash: 51875b12244a6e2fb427c27d7fece6fae9833c03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601247"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitraums zurück. 
  
## <a name="quick-info"></a>QuickInfo

Siehe [IFreeBusySupport](ifreebusysupport.md).
  
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

_Cmax_
  
> [in] Die Anzahl der [zurückzugebenden IFreeBusyData-Schnittstellen.](ifreebusydata.md) 
    
_rwgbuser_
  
> [in] Das Array von Frei/Gebucht-Benutzern, für die Daten abgerufen werden sollen.
    
_prwgbdata_
  
> [in] [out] Das Array von **IFreeBusyData-Schnittstellen,** die dem  _Rfgbuser-Array_ von [FBUser-Strukturen](fbuser.md) entsprechen. 
    
   > [!NOTE]
   > Dieses Array von Zeigern wird vom Aufrufer zugewiesen und vom Aufrufer freigegeben. Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer damit fertig ist. 
  
_phrStatus_
  
> [out] Das Array der **HRESULT-Ergebnisse** zum Abrufen jeder entsprechenden **IFreeBusyData-Schnittstelle.** Der Wert kann NULL sein. Ein Ergebnis wird auf S_OK festgelegt, wenn entsprechende  _Prwgbdata_ gültig sind. 
    
_pcRead_
  
>  [out] Die tatsächliche Anzahl der Benutzer, für die eine **IFreeBusyData-Schnittstelle** gefunden wurde. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)

