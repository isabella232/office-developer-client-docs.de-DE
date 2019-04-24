---
title: XML-Beispiel für Aktivitätsfeeds
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: 'Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge für Aktivitätsfeeds, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die ISocialSession2:: GetActivitiesEx-Methode für ein soziales Netzwerk aufgerufen wurde.'
ms.openlocfilehash: 6370b559c5160bfa48d32afa77715e9a7c126aab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281332"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="423e0-103">XML-Beispiel für Aktivitätsfeeds</span><span class="sxs-lookup"><span data-stu-id="423e0-103">Activity Feed XML Example</span></span>

<span data-ttu-id="423e0-104">Das XML-Beispiel in diesem Thema ist eine XML-Zeichenfolge für Aktivitätsfeeds, die an den Outlook Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode für ein soziales Netzwerk aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="423e0-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="423e0-105">Das Beispiel zeigt den **activityFeed** -XML-Code, der die folgenden vier Aktivitäten enthält, die jeweils durch das **activityDetails** -Element und das Zuordnen einer Vorlage zu Anzeigezwecken getrennt sind:</span><span class="sxs-lookup"><span data-stu-id="423e0-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="423e0-106">Eine Profilbild Aktualisierung von Melissa Macbeth, deren **Besitzerin** im sozialen Netzwerk 4667647 ist.</span><span class="sxs-lookup"><span data-stu-id="423e0-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="423e0-107">Diese Aktivität gibt drei Vorlage Variablen vom Typ **publisherVariable**, **listVariable**und **pictureVariable** (die in **listVariable**eingeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="423e0-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="423e0-108">Diese Variablen geben die Person an, die das Aktivitätsfeed-Element veröffentlicht hat, sowie Informationen für das zu aktualisierende Bild (mithilfe der untergeordneten Elemente **Name**, **value**, **altText**und **href** von **pictureVariable**).</span><span class="sxs-lookup"><span data-stu-id="423e0-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="423e0-109">Eine Profilbild Aktualisierung von Michael affronti, \*\*\*\* deren Besitzerin im sozialen Netzwerk 5015012 ist.</span><span class="sxs-lookup"><span data-stu-id="423e0-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="423e0-110">Ähnlich wie bei der letzten Aktivität gibt diese Aktivität drei Vorlagenvariablen vom Typ **publisherVariable**, **listVariable**und **pictureVariable**an.</span><span class="sxs-lookup"><span data-stu-id="423e0-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="423e0-111">Diese Variablen geben die Person an, die das Aktivitätsfeed-Element veröffentlicht hat, und Informationen für das zu aktualisierende Bild.</span><span class="sxs-lookup"><span data-stu-id="423e0-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="423e0-112">Eine Statusaktualisierung von Michael affronti mit derselben **Besitzer** -und 5015012 wie die letzte Aktivität.</span><span class="sxs-lookup"><span data-stu-id="423e0-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="423e0-113">Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **publisherVariable** und **Textvariable**an.</span><span class="sxs-lookup"><span data-stu-id="423e0-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="423e0-114">**publisherVariable** gibt die Person an, die das Aktivitätsfeed-Element \*\*\*\* veröffentlicht hat, und Textvariable enthält einen **Wert** der Status Position.`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="423e0-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="423e0-115">Ein Blogbeitrag von Michael affronti mit derselben **Besitzer** -und 5015012 wie die letzten beiden Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="423e0-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="423e0-116">Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **publisherVariable** und **linkVariable**an.</span><span class="sxs-lookup"><span data-stu-id="423e0-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="423e0-117">**publisherVariable** gibt die Person an, die das Aktivitäts Feedelement veröffentlicht hat, und **linkVariable** enthält weitere Informationen (angegeben durch die untergeordneten Elemente " **Name**", " **Text**" und " **value** " von **linkVariable**) über den Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="423e0-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="423e0-118">Jede der vier Aktivitäten gibt einen **Vorlagen** -Wert an, der mit einer der drei Vorlagen übereinstimmt, die im **Templates** -Element angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="423e0-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="423e0-119">Jede Vorlage befindet sich in einem eigenen **activityTemplateContainer** -Element, das durch einen **Template** -Wert identifiziert wird, der auch zum Anzeigen einer Aktivität verwendet wird, die den gleichen **Vorlagen** -Wert hat.</span><span class="sxs-lookup"><span data-stu-id="423e0-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="423e0-120">Eine ausführliche Beschreibung der im Beispiel verwendeten XML-Elemente finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="423e0-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="423e0-121">Übersicht über XML für ein Aktivitäts Feed-Element</span><span class="sxs-lookup"><span data-stu-id="423e0-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="423e0-122">activityDetails-Element</span><span class="sxs-lookup"><span data-stu-id="423e0-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="423e0-123">activityTemplateContainer-Element</span><span class="sxs-lookup"><span data-stu-id="423e0-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="423e0-124">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="423e0-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="423e0-125">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="423e0-125">XML example</span></span>

<span data-ttu-id="423e0-126">Das folgende Beispiel zeigt die **activityFeed** -XML von vier Aktivitäten: zwei Profilbild Aktualisierungen, eine Statusaktualisierung und einen Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="423e0-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="423e0-127">Der XML-Code gibt außerdem drei Aktivitätsanzeige Vorlagen für die Anzeige der entsprechenden Aktivitäten an.</span><span class="sxs-lookup"><span data-stu-id="423e0-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="423e0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="423e0-128">See also</span></span>

- [<span data-ttu-id="423e0-129">OSC-Anbieter-XML-Beispiele</span><span class="sxs-lookup"><span data-stu-id="423e0-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="423e0-130">XML für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="423e0-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="423e0-131">XML-Beispiel für Funktionen</span><span class="sxs-lookup"><span data-stu-id="423e0-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="423e0-132">XML-Beispiel für Freunde</span><span class="sxs-lookup"><span data-stu-id="423e0-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="423e0-133">XML-Schema des Anbieters für soziale Netzwerke in Outlook</span><span class="sxs-lookup"><span data-stu-id="423e0-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

