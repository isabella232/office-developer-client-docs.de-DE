---
title: Beispielcode für die Einschränkung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b82097c-dbd6-4ba0-a6cb-292301f9402b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f41abe2ee41946f68e1d79c75b36791364ea970
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795409"
---
# <a name="sample-restriction-code"></a><span data-ttu-id="a41a2-103">Beispielcode für die Einschränkung</span><span class="sxs-lookup"><span data-stu-id="a41a2-103">Sample restriction code</span></span>

<span data-ttu-id="a41a2-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a41a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a41a2-105">Der folgende Beispielcode zeigt, wie eine Einschränkung erstellen, die alle Nachrichten herausgefiltert, die nicht das Wort enthalten "Volleyball" in der Betreffzeile und nicht an Sue von Sam gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a41a2-105">The following sample code shows how to create a restriction that filters out all messages that do not contain the word "volleyball" in the subject line and were not sent to Sue from Sam.</span></span> <span data-ttu-id="a41a2-106">Eine Struktur von [SRestriction](srestriction.md) Strukturen ist erforderlich, mit den obersten Knoten, der eine Einschränkung des **und** mit einer [SAndRestriction](sandrestriction.md) Struktur implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a41a2-106">A tree of [SRestriction](srestriction.md) structures is required, with the top node being an **AND** restriction implemented with an [SAndRestriction](sandrestriction.md) structure.</span></span> <span data-ttu-id="a41a2-107">Die drei Einschränkungen, die von der **AND** -Operation verbunden sind werden eine Unterobjekts Einschränkung, die für Nachrichten an Sue sucht, einen Content-Beschränkung, die für Nachrichten von Sam durchsucht und eine andere **und** Einschränkung, die nach Nachrichten gesucht haben einen Betreff mit "Volleyball."</span><span class="sxs-lookup"><span data-stu-id="a41a2-107">The three restrictions that are joined by the **AND** operation are a subobject restriction that searches for messages sent to Sue, a content restriction that searches for messages from Sam, and another **AND** restriction that searches for messages that have a subject containing "volleyball."</span></span> <span data-ttu-id="a41a2-108">Da **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) keine erforderliche Eigenschaft ist, muss eine Einschränkung **vorhanden** eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a41a2-108">Because **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) is not a required property, an **Exist** restriction must be included.</span></span> 
  
<span data-ttu-id="a41a2-109">In diesem Code wird die dynamische Zuweisung und Initialisierung; Es ist möglich, reservieren und statisch sowie zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a41a2-109">This code uses dynamic allocation and initialization; it is possible to allocate and initialize statically as well.</span></span> <span data-ttu-id="a41a2-110">Um das Beispiel abzukürzen die fehlerprüfung, die in der folgenden auftreten muss die Aufrufe der Zuordnung ist nicht enthalten in der Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="a41a2-110">In the interest of brevity, the error checking that must occur following the allocation calls is not included in the sample.</span></span> 
  
```cpp
HRESULT BuildRestriction (LPSTR pszSent, LPSTR pszFrom,
                                LPSTR pszSubjectText);
{
    LPSRestriction pRest, pAndRes, pObjRes, pSubjAndRes;
    LPSPropValue pRecip, pSender, pSubject;
    HRESULT hResult;
    ULONG ulResCount = 3, ulSubjCount = 2
    // Allocate and build  restriction to join criteria
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulResCount, pRest,
            (LPVOID *)&pAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Allocate and build subobject restriction to search recipient list
    hResult = MAPIAllocateMore (sizeof(SRestriction), pRest,
            (LPVOID *)&pObjRes);
    pAndRes[0].rt = RES_SUBRESTRICTION;
    pAndRes[0].res.resSub.ulSubObject = PR_MESSAGE_RECIPIENTS;
    pAndRes[0].res.resSub.lpRes = pObjRes;
    // Allocate and build content restriction to look for recipient
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pRecip);
    pObjRes->rt = RES_CONTENT;
    pObjRes->res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pObjRes->res.resContent.ulPropTag = pRecip->ulPropTag =
            PR_DISPLAY_NAME;
    pObjRes->res.resContent.lpProp = pRecip;
    pRecip->Value.LPSZ = pszSent;              // pszSent set to Sue
    // Allocate and build content restriction to look for sender
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSend);
    pAndRes[1].rt = RES_CONTENT;
    pAndRes[1].res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pAndRes[1].res.resContent.ulPropTag = pSend->ulPropTag =
            PR_SENDER_NAME;
    pAndRes[1].res.resContent.lpProp = pSend;
    pSend->Value.LPSZ = pszName;                    // pszName set to Sam
    // Allocate and build  restriction to look for subject
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulSubjCount, pRest,
            (LPVOID *)&pSubjAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Create an  restriction to search for subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubjAndRes);
    pAndRes[2].rt = RES_AND;
    pAndRes[2].res.resAnd.cRes = ulSubjCount;
    pAndRes[2].res.resAnd.lpRes = pSubjAndRes;
    // Exist restriction to check that PR_SUBJECT exists
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[0].rt = RES_EXIST;
    pSubjAndRes[0].res.resExist.ulReserved1 = 0;
    pSubjAndRes[0].res.resExist.ulReserved2 = 0;
    pSubjAndRes[0].res.resExist.ulPropTag = PR_SUBJECT;
    // Content restriction to check for "volleyball" in subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[1].res.resContent.ulFuzzyLevel =
            FL_SUBSTRING | FL_IGNORECASE;
    pSubjAndRes[1].res.resContent.ulPropTag = pSubj->ulPropTag =
            PR_SUBJECT;
    pSubjAndRes[1].res.resContent.lpProp = pSubj;
    pSubj->Value.LPSZ = pszSubjectText;
    return hResult;
}
 
```

## <a name="see-also"></a><span data-ttu-id="a41a2-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a41a2-111">See also</span></span>

- [<span data-ttu-id="a41a2-112">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="a41a2-112">MAPI Tables</span></span>](mapi-tables.md)

