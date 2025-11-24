# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
Stability analysis of a control system using the Bode plot is based on evaluating the gain margin, phase margin, and their corresponding crossover frequencies from the frequency response of the open-loop transfer function.

For the given system 𝐺(𝑠)=1/𝑠(1+0.5𝑠)(1+0.1𝑠), the Bode plot helps determine how the magnitude and phase vary over a range of frequencies.

The phase margin indicates how close the system is to becoming unstable, while the gain margin shows how much gain variation the system can tolerate before instability occurs.

If both margins are positive, the closed-loop system is considered stable.

MATLAB is used to verify the theoretical stability by generating the Bode plot, computing margins, and confirming whether the system satisfies stability criteria.



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end

```

## Output:
<img width="657" height="499" alt="image" src="https://github.com/user-attachments/assets/d58f7837-6fc2-4345-a472-894f2d204723" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12
Phase Margin = 60
Gain crossover frequency = 0.907
Phase crossover frequency = 4.4721.

The system is stable.
