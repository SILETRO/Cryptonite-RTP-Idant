# Weather Forecasting

## Pre-processing

- Created distinct columns for date, month, and year
- Converted date to a periodic cyclic signal for better recognition of seasonal patterns
- Converted wind speed and direction into vectors
- Created separate columns to capture weekly and monthly rolling average of temperature and precipitation
- Created a 30-day window size in order to best capture monthly patterns

## Model Development

### Univariate Model

Built three distinct baseline models using SimpleRNN, LSTM, and GRU architectures.

- GRU gave the most accurate outputs among all three models

### Multivariate Model

Built three distinct models using SimpleRNN, LSTM, and GRU architectures.

- GRU again gave the most accurate output among all three models

## Performance Comparison

### Temperature Prediction

| Model Type | MAE | RMSE |
|------------|-----|------|
| Univariate | 1.21 | 1.58 |
| Multivariate | 0.39 | 0.52 |

### Precipitation Prediction

| Model Type | MAE | RMSE |
|------------|------|-------|
| Univariate | 23.15 | 26.28 |
| Multivariate | 6.80 | 15.04 |

The GRU architecture provided the best results across both univariate and multivariate approaches.
<img width="2391" height="624" alt="image" src="https://github.com/user-attachments/assets/e157f94e-048b-45a6-81c7-8e7572caf852" />
<img width="2400" height="624" alt="image" src="https://github.com/user-attachments/assets/39a16a16-0fcd-41ed-b358-f9f872d309af" />

## The Office Generator

- Total vocabulary size: 73
- Total characters: 3427466
- Context Length: 300
<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/7df3a8e2-a951-4eec-aa55-e1706ddf4af5" />
<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/d90d324e-624e-498d-b3c2-01aa5974f909" />

### Best sample
- Temperature Used: 0.5
- Perplexity: 1.73
- Seed text: "Michael: "
### Generation

Michael: I was thinking about something about the most dogs to get this thing.

Jim:  Hey, Jim. I am going to be done a movie and I can't present the food side.

Andy: I know what they say. And I brought with us about closing the company. And then I was a little expective to my brother was to be able to talk about that Oscar. I guess I can get you to see her eyes and you are saying you think that you are fine. I was hoping that I would complain in the mail country and I'm completely nice to me. And I have a company that you have a very busy man. And I was just going to be a big deal with a more personal straight. And he made the great thing on the other thing in a corner. So the story were better than anyone who would be a woman here. And I want to say that it was a complete surget of the house. I was in the warehouse. The only one was the only thing that we have come to my private to a website.

Andy: Yeah.

Dwight: The guns was important to the five minutes and I will be out of my head. I have a very looking at my car. I am not going to be there. I think I was a great state.

Michael:  Hey, hey, hey, hey! She's got a bad thing.

Michael: Hey.

Dwight: All right, so I have an announcement that you can do this in the company.

Angela: Well, that's not about the way I could do it and have to prove him and he says that, so maybe we shouldn't have throw them on the parking lot. She was just a training statement.

Michael: Okay.

Michael: Good. Good. There is no way that I was thinking about this business. And then we are going to be paying for the party, which is with your car. This is where I was a chance. And I was saying some time in the conference room and find out and they don't even have the office to do something that I can do is a point of a paper company. I will do that. I can't do this.

Dwight: Yeah. I was just not an approval of the board with the sales call about home. This is a business completely consideration of the way he has a business this weekend. I was hoping that was a good promotion.

Michael: I can't do this no shot!  I'm sorry, I don't know what that is. I know how to do it. I know what you were having any more right now. It's not a stupid card. And I would like to have some completely reasons to start the face of the paper company.

Kevin: Five minutes and I have no idea. I have to go to the most idea and he has a great slage for you. And I was gonna go to the Scranton branch.

Stanley: No, no. No. No. I am the perfect salesman in the conference room.

Michael: No, you know what? That is not a computer. That's what you said.

Dwight: You know what? I am sure that you can see them who doesn't like these little cards and they're gonna kill me. I'm sorry.

Roy: You know what? I am not the way I can get this into a toy life with this.

Dwight: Michael was a party in the back of people and I was a big one policy. I was saying that I was just trying to... I mean, I am not gonna get all the bus down to the bathroom.

Pam: It's good. We are going to be a mome
