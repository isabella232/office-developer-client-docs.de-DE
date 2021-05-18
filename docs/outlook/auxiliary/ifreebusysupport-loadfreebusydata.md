---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitbereichs zurück.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411232"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Gibt für jeden angegebenen Benutzer eine Schnittstelle zum Aufzählen von Frei/Gebucht-Datenblöcken innerhalb eines Zeitbereichs zurück. 
  
## <a name="quick-info"></a>QuickInfo

Weitere [Informationen finden Sie unter IFreeBusySupport](ifreebusysupport.md).
  
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
  
> [in] Die Anzahl der [zurückzukehrende IFreeBusyData-Schnittstellen.](ifreebusydata.md) 
    
_rgfbuser_
  
> [in] Das Array der Frei/Gebucht-Benutzer, für die Daten abgerufen werden.
    
_prgfbdata_
  
> [in] [out] Das Array von **IFreeBusyData-Schnittstellen,** die dem  _rgfbuser-Array_ von [FBUser-Strukturen](fbuser.md) entsprechen. 
    
   > [!NOTE]
   > Dieses Array von Zeigern wird vom Anrufer zugewiesen und vom Anrufer frei. Die tatsächlichen Schnittstellen, auf die verwiesen wird, werden freigegeben, wenn der Aufrufer damit fertig ist. 
  
_phrStatus_
  
> [out] Das Array von **HRESULT-Ergebnissen** zum Abrufen jeder entsprechenden **IFreeBusyData-Schnittstelle.** Der Wert kann NULL sein. Ein Ergebnis wird auf S_OK festgelegt, wenn  _entsprechende prgfbdata_ gültig ist. 
    
_pcRead_
  
>  [out] Die tatsächliche Anzahl von Benutzern, für die eine **IFreeBusyData-Schnittstelle** gefunden wurde. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Frei/Gebucht-API)](constants-free-busy-api.md)

