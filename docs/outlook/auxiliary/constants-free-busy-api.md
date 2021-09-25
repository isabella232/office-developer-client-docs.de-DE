---
title: Konstanten (Frei/Gebucht-API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Dieses Thema enthält Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.
ms.openlocfilehash: 429c5c5d402a8239b575271dc052dd32bf29b96f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592823"
---
# <a name="constants-freebusy-api"></a>Konstanten (Frei/Gebucht-API)

Dieses Thema enthält Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.
  
## <a name="constants"></a>Konstanten

|**Konstante**|**Definition**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Wie in der Windows SDK-Headerdatei winerror.h definiert.*  <br/> |
|S_FALSE  <br/> | *Wie in der Windows SDK-Headerdatei winerror.h definiert.*  <br/> |
|S_OK  <br/> | *Wie in der Windows SDK-Headerdatei winerror.h definiert.*  <br/> |
   
## <a name="interface-identifiers"></a>Schnittstellenbezeichner

Bei den folgenden Schnittstellenbezeichnern wird davon ausgegangen, dass das in der Windows SDK-Headerdatei guiddef.h definierte DEFINE_GUID Makro dem Wert des symbolischen GUID-Namens zugeordnet wird.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

