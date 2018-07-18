---
title: XML-Beispiel für „friends“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: Das XML-Beispiel in diesem Thema ist eine Friend-XML-Zeichenfolge an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die ISocialPerson::GetFriendsAndColleagues-Methode aufgerufen. Das Beispiel zeigt die Freunde XML für zwei Freunde, jeweils durch das Element Person sind. Jeder Freund gibt einen eindeutigen Wert für das UserID-Element im sozialen Netzwerk.
ms.openlocfilehash: 6944213e9483042862fa4cefd8420e39ade9139f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795949"
---
# <a name="friends-xml-example"></a><span data-ttu-id="24fc9-105">XML-Beispiel für „friends“</span><span class="sxs-lookup"><span data-stu-id="24fc9-105">Friends XML example</span></span>

<span data-ttu-id="24fc9-106">Das XML-Beispiel in diesem Thema ist eine Friend-XML-Zeichenfolge an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="24fc9-107">Das Beispiel zeigt die **Freunde** XML für zwei Freunde, jeweils durch das Element **Person** sind.</span><span class="sxs-lookup"><span data-stu-id="24fc9-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="24fc9-108">Jeder Freund gibt einen eindeutigen Wert für das **UserID** -Element im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="24fc9-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="24fc9-109">Die verbleibenden Elemente der **Freunde** XML haben selbsterklärend Namen.</span><span class="sxs-lookup"><span data-stu-id="24fc9-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="24fc9-110">Detaillierte Beschreibung dieser Elemente finden Sie unter [XML für Freunde](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="24fc9-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="24fc9-111">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="24fc9-111">XML example</span></span>

<span data-ttu-id="24fc9-112">Das folgende Beispiel zeigt die **Freunde** XML für zwei Personen im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="24fc9-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>http://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>http://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a><span data-ttu-id="24fc9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24fc9-113">See also</span></span>

- [<span data-ttu-id="24fc9-114">OSC-Anbieter XML-Beispielen</span><span class="sxs-lookup"><span data-stu-id="24fc9-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="24fc9-115">Funktionen XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="24fc9-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="24fc9-116">Beispiel für eine Aktivität Feed XML</span><span class="sxs-lookup"><span data-stu-id="24fc9-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="24fc9-117">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="24fc9-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

